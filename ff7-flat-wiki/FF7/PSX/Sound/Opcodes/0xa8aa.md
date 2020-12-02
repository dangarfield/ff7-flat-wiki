---
title: 0xa8aa
---

[Home](/ff7-flat-wiki/Main%20Page.md) > [FF7](/ff7-flat-wiki/FF7.md) > [PSX](/ff7-flat-wiki/FF7/PSX.md) > [Sound](/ff7-flat-wiki/FF7/PSX/Sound.md) > [Opcodes](/ff7-flat-wiki/FF7/PSX/Sound/Opcodes.md) > 0xa8aa

## 0xA8, 0xAA, 0xA3 (Channel Volume, Pan, Volume Modifier)

0xA8 has one 8-bit parameter, which used in calculation of base channel
volume.

0xAA has one 8-bit parameter, which used in calculation of channel pan
(difference between left and right channel volume).

0xA3 has one 8-bit parameter, which used in calculation of base channel
volume.

### Volume Calculation

`// m_AKAO_VOLUME_TABLE_L[i] = 32768 - m_AKAO_VOLUME_TABLE_R[i];`  
`const uint16_t m_AKAO_VOLUME_TABLE_L[128] = {`  
`  0x7f80, 0x7e80, 0x7d80, 0x7c80, 0x7b80, 0x7a80, 0x7980, 0x7880,`  
`  0x7780, 0x7680, 0x7580, 0x7480, 0x7380, 0x7280, 0x7180, 0x7080,`  
`  0x6f80, 0x6e80, 0x6d80, 0x6c80, 0x6b80, 0x6a80, 0x6980, 0x6880,`  
`  0x6780, 0x6680, 0x6580, 0x6480, 0x6380, 0x6280, 0x6180, 0x6080,`  
`  0x5f80, 0x5e80, 0x5d80, 0x5c80, 0x5b80, 0x5a80, 0x5980, 0x5880,`  
`  0x5780, 0x5680, 0x5580, 0x5480, 0x5380, 0x5280, 0x5180, 0x5080,`  
`  0x4f80, 0x4e80, 0x4d80, 0x4c80, 0x4b80, 0x4a80, 0x4980, 0x4880,`  
`  0x4780, 0x4680, 0x4580, 0x4480, 0x4380, 0x4280, 0x4180, 0x4080,`  
`  0x3f80, 0x3e80, 0x3d80, 0x3c80, 0x3b80, 0x3a80, 0x3980, 0x3880,`  
`  0x3780, 0x3680, 0x3580, 0x3480, 0x3380, 0x3280, 0x3180, 0x3080,`  
`  0x2f80, 0x2e80, 0x2d80, 0x2c80, 0x2b80, 0x2a80, 0x2980, 0x2880,`  
`  0x2780, 0x2680, 0x2580, 0x2480, 0x2380, 0x2280, 0x2180, 0x2080,`  
`  0x1f80, 0x1e80, 0x1d80, 0x1c80, 0x1b80, 0x1a80, 0x1980, 0x1880,`  
`  0x1780, 0x1680, 0x1580, 0x1480, 0x1380, 0x1280, 0x1180, 0x1080,`  
`  0x0f80, 0x0e80, 0x0d80, 0x0c80, 0x0b80, 0x0a80, 0x0980, 0x0880,`  
`  0x0780, 0x0680, 0x0580, 0x0480, 0x0380, 0x0280, 0x0180, 0x0080`  
`};`  
  
`// m_AKAO_VOLUME_TABLE_R[i] = i * 256 + 128;`  
`const uint16_t m_AKAO_VOLUME_TABLE_R[128] = {`  
`  0x0080, 0x0180, 0x0280, 0x0380, 0x0480, 0x0580, 0x0680, 0x0780,`  
`  0x0880, 0x0980, 0x0a80, 0x0b80, 0x0c80, 0x0d80, 0x0e80, 0x0f80,`  
`  0x1080, 0x1180, 0x1280, 0x1380, 0x1480, 0x1580, 0x1680, 0x1780,`  
`  0x1880, 0x1980, 0x1a80, 0x1b80, 0x1c80, 0x1d80, 0x1e80, 0x1f80,`  
`  0x2080, 0x2180, 0x2280, 0x2380, 0x2480, 0x2580, 0x2680, 0x2780,`  
`  0x2880, 0x2980, 0x2a80, 0x2b80, 0x2c80, 0x2d80, 0x2e80, 0x2f80,`  
`  0x3080, 0x3180, 0x3280, 0x3380, 0x3480, 0x3580, 0x3680, 0x3780,`  
`  0x3880, 0x3980, 0x3a80, 0x3b80, 0x3c80, 0x3d80, 0x3e80, 0x3f80,`  
`  0x4080, 0x4180, 0x4280, 0x4380, 0x4480, 0x4580, 0x4680, 0x4780,`  
`  0x4880, 0x4980, 0x4a80, 0x4b80, 0x4c80, 0x4d80, 0x4e80, 0x4f80,`  
`  0x5080, 0x5180, 0x5280, 0x5380, 0x5480, 0x5580, 0x5680, 0x5780,`  
`  0x5880, 0x5980, 0x5a80, 0x5b80, 0x5c80, 0x5d80, 0x5e80, 0x5f80,`  
`  0x6080, 0x6180, 0x6280, 0x6380, 0x6480, 0x6580, 0x6680, 0x6780,`  
`  0x6880, 0x6980, 0x6a80, 0x6b80, 0x6c80, 0x6d80, 0x6e80, 0x6f80,`  
`  0x7080, 0x7180, 0x7280, 0x7380, 0x7480, 0x7580, 0x7680, 0x7780,`  
`  0x7880, 0x7980, 0x7a80, 0x7b80, 0x7c80, 0x7d80, 0x7e80, 0x7f80`  
`};`  
  
`left_volume = m_AKAO_VOLUME_TABLE_L[aa_parameter] * ((a8_parameter * a3_parameter * 0x7f) / 128) / 256 / 128;`  
  
`right_volume = m_AKAO_VOLUME_TABLE_R[aa_parameter] * ((a8_parameter * a3_paramater * 0x7f) / 128) / 256 / 128;`

If there is no A3 opcode in sequence (as in SENSUI.SND for example),
default value 0x7f is used.

If there is no A8 opcode in sequence, default value 0x7f.fe is used.
(More precisely, 0x3fff is stored in memory.)