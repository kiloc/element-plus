## Descriptions

Display multiple fields in list form.

### Basic usage

:::demo

```html
<el-descriptions title="User Info">
  <el-descriptions-item label="Username">kooriookami</el-descriptions-item>
  <el-descriptions-item label="Telephone">18100000000</el-descriptions-item>
  <el-descriptions-item label="Place">Suzhou</el-descriptions-item>
  <el-descriptions-item label="Remarks">
    <el-tag size="small">School</el-tag>
  </el-descriptions-item>
  <el-descriptions-item label="Address"
    >No.1188, Wuzhong Avenue, Wuzhong District, Suzhou, Jiangsu
    Province</el-descriptions-item
  >
</el-descriptions>
```

:::

### Sizes

:::demo

```html
<template>
  <el-radio-group v-model="size">
    <el-radio label="">Default</el-radio>
    <el-radio label="medium">Medium</el-radio>
    <el-radio label="small">Small</el-radio>
    <el-radio label="mini">Mini</el-radio>
  </el-radio-group>

  <el-descriptions
    class="margin-top"
    title="With border"
    :column="3"
    :size="size"
    border
  >
    <template #extra>
      <el-button type="primary" size="small">Operation</el-button>
    </template>
    <el-descriptions-item>
      <template #label>
        <i class="el-icon-user"></i>
        Username
      </template>
      kooriookami
    </el-descriptions-item>
    <el-descriptions-item>
      <template #label>
        <i class="el-icon-mobile-phone"></i>
        Telephone
      </template>
      18100000000
    </el-descriptions-item>
    <el-descriptions-item>
      <template #label>
        <i class="el-icon-location-outline"></i>
        Place
      </template>
      Suzhou
    </el-descriptions-item>
    <el-descriptions-item>
      <template #label>
        <i class="el-icon-tickets"></i>
        Remarks
      </template>
      <el-tag size="small">School</el-tag>
    </el-descriptions-item>
    <el-descriptions-item>
      <template #label>
        <i class="el-icon-office-building"></i>
        Address
      </template>
      No.1188, Wuzhong Avenue, Wuzhong District, Suzhou, Jiangsu Province
    </el-descriptions-item>
  </el-descriptions>

  <el-descriptions
    class="margin-top"
    title="Without border"
    :column="3"
    :size="size"
  >
    <template #extra>
      <el-button type="primary" size="small">Operation</el-button>
    </template>
    <el-descriptions-item label="Username">kooriookami</el-descriptions-item>
    <el-descriptions-item label="Telephone">18100000000</el-descriptions-item>
    <el-descriptions-item label="Place">Suzhou</el-descriptions-item>
    <el-descriptions-item label="Remarks">
      <el-tag size="small">School</el-tag>
    </el-descriptions-item>
    <el-descriptions-item label="Address"
      >No.1188, Wuzhong Avenue, Wuzhong District, Suzhou, Jiangsu
      Province</el-descriptions-item
    >
  </el-descriptions>
</template>

<script>
  export default {
    data() {
      return {
        size: '',
      }
    },
  }
</script>
```

:::

### Vertical List

:::demo

```html
<el-descriptions
  title="Vertical list with border"
  direction="vertical"
  :column="4"
  border
>
  <el-descriptions-item label="Username">kooriookami</el-descriptions-item>
  <el-descriptions-item label="Telephone">18100000000</el-descriptions-item>
  <el-descriptions-item label="Place" :span="2">Suzhou</el-descriptions-item>
  <el-descriptions-item label="Remarks">
    <el-tag size="small">School</el-tag>
  </el-descriptions-item>
  <el-descriptions-item label="Address"
    >No.1188, Wuzhong Avenue, Wuzhong District, Suzhou, Jiangsu
    Province</el-descriptions-item
  >
</el-descriptions>

<el-descriptions
  class="margin-top"
  title="Vertical list without border"
  :column="4"
  direction="vertical"
>
  <el-descriptions-item label="Username">kooriookami</el-descriptions-item>
  <el-descriptions-item label="Telephone">18100000000</el-descriptions-item>
  <el-descriptions-item label="Place" :span="2">Suzhou</el-descriptions-item>
  <el-descriptions-item label="Remarks">
    <el-tag size="small">School</el-tag>
  </el-descriptions-item>
  <el-descriptions-item label="Address"
    >No.1188, Wuzhong Avenue, Wuzhong District, Suzhou, Jiangsu
    Province</el-descriptions-item
  >
</el-descriptions>
```

:::

### Customized Style

:::demo

```html
<el-descriptions title="Customized style list" :column="3" border>
  <el-descriptions-item
    label="Username"
    label-align="right"
    align="center"
    label-class-name="my-label"
    class-name="my-content"
    width="150px"
    >kooriookami</el-descriptions-item
  >
  <el-descriptions-item label="Telephone" label-align="right" align="center"
    >18100000000</el-descriptions-item
  >
  <el-descriptions-item label="Place" label-align="right" align="center"
    >Suzhou</el-descriptions-item
  >
  <el-descriptions-item label="Remarks" label-align="right" align="center">
    <el-tag size="small">School</el-tag>
  </el-descriptions-item>
  <el-descriptions-item label="Address" label-align="right" align="center"
    >No.1188, Wuzhong Avenue, Wuzhong District, Suzhou, Jiangsu
    Province</el-descriptions-item
  >
</el-descriptions>
```

:::

### Descriptions Attributes

| Attribute | Description                                | Type    | Accepted Values       | Default    |
| --------- | ------------------------------------------ | ------- | --------------------- | ---------- |
| border    | with or without border                     | boolean | —                     | false      |
| column    | numbers of `Descriptions Item` in one line | number  | —                     | 3          |
| direction | direction of list                          | string  | vertical / horizontal | horizontal |
| size      | size of list                               | string  | medium / small / mini | —          |
| title     | title text, display on the top left        | string  | —                     | —          |
| extra     | extra text, display on the top right       | string  | —                     | —          |

### Descriptions Slots

| Name  | Description                                 |
| ----- | ------------------------------------------- |
| title | custom title, display on the top left       |
| extra | custom extra area, display on the top right |

### Descriptions Item Attributes

| Attribute        | Description                                                                                                                                                                                  | Type            | Accepted Values       | Default |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------- | --------------------- | ------- |
| label            | label text                                                                                                                                                                                   | string          | —                     | —       |
| span             | colspan of column                                                                                                                                                                            | number          | —                     | 1       |
| width            | column width, the width of the same column in different rows is set by the max value (If no `border`, width contains label and content)                                                      | string / number | —                     | —       |
| min-width        | column minimum width, columns with `width` has a fixed width, while columns with `min-width` has a width that is distributed in proportion (If no`border`, width contains label and content) | string / number | —                     | —       |
| align            | column content alignment (If no `border`, effective for both label and content)                                                                                                              | string          | left / center / right | left    |
| label-align      | column label alignment, if omitted, the value of the above `align` attribute will be applied (If no `border`, please use `align` attribute)                                                  | string          | left / center / right | —       |
| class-name       | column content custom class name                                                                                                                                                             | string          | —                     | —       |
| label-class-name | column label custom class name                                                                                                                                                               | string          | —                     | —       |

### Descriptions Item Slots

| Name  | Description  |
| ----- | ------------ |
| label | custom label |
