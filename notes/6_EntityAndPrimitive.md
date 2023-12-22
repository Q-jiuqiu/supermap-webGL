<!--
 * @Author: quling
 * @Date: 2023-12-22 11:24:07
 * @LastEditors: quling
 * @LastEditTime: 2023-12-22 14:35:34
 * @Description: 
 * @FilePath: \supermap-webGL\notes\6_EntityAndPrimitive.md
-->
# [entity 与 primitive区别](https://blog.csdn.net/weixin_45782925/article/details/122690683)
Cesium为开发者提供了丰富的图形绘制和空间数据管理的API，可以分为两类:
  1. 一类是面向图形开发人员的低层次API，通常被称为Primitive API
  2. 一类是用于驱动数据可视化的高层次API，称为Entity API
## Entity
Entity是对Primitive的封装
材质使用——MaterialProperty
## Primitive
由两部分组成：
  1. 几何形状——Geometry，定义Primitive的结构，例如点、线、面、体等
  2. 外观——Appearance，定义Primitive的着色
材质使用——Material
优点:
  1. 高性能，绘制大量Primitive时，可以将其合并为单个Geometry，
	2. 灵活性，Geometry与Appearance相互独立
绘制步骤：
  1. 创建Geometry对象——Geometry
  2. 定义几何形状——GeometryInstance
  3. 定义外观——Material
  4. 创建Primitive