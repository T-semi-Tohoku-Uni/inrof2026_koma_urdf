# inrof2026_koma_urdf

```bash
sed -i "s|\$(find assembly_main_description)|$(pwd)|g" urdf/materials.xacro urdf/assembly_main.xacro
uv run xacro urdf/assembly_main.xacro > urdf/komarm.urdf
sed -i 's|package://assembly_main_description/|../|g' urdf/komarm.urdf
```