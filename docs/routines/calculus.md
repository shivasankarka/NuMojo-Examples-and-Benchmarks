

## Differentiation

5. **`numojo.gradient[in_dtype: DType, out_dtype: DType = DType.float32](x: NDArray[in_dtype], spacing: Scalar[in_dtype]) -> NDArray[dtype]`**

Return the gradient of a 1D array (Future updates will include axis argument).

### Inputs

| **Parameter** | **Description**                | **Type** |
| ------------- | ------------------------------ | -------- |
| `in_dtype`    | Datatype of the input elements  | DType    |
| `out_dtype`   | Datatype of the output elements | DType    |

| **Args**     | **Description**                                             | **Type**          |
| ------------ | ----------------------------------------------------------- | ----------------- |
| `x`      | Array whose gradient will be calculated | `NDArray` |
| `spacing`      | Scalar value representing the spacing between each value in domain of x. | `Scalar[in_dtype]` |


### Example
```python
    import numojo as nj
    var arr = nj.NDArray[nj.f32](data=List[SIMD[numojo.f32, 1]](1.0, 2.0, 4.0, 7.0, 11.0, 16.0),
    shape=List[Int](6))
    var result = nj.differentiation.gradient[numojo.f32](arr, spacing=1.0)
    print(result) # prints the resultant gradient of arr
```

---

<br>

## trapz 