# MetahumVisemeCurves

This is simple Pose Asset with visemes for Epic's MetaHuman face skeleton. I used it for my Lip-Sync plugin:
https://www.youtube.com/watch?v=cQQjDYZpMZ4

* mh_lipsync_mapping_anim - source animation
* PA_Metahuman_Lipsync - pose asset with 12 visemes:

AA - LS_A

SH, CH, ZH - LS_SH

I - LS_IH

O - LS_OH

UW - LS_U

B, M, P - LS_B

F, V - LS_V

D, S, T, L - LS_D

E - LS_Eh

G, K - LS_G

N - LS_N

R - LS_R

1. Import MetaHuman character to your UE4 project.

2. Open MetahumVisemeCurves project.

3. In Content Browser under [Content/MetaHumans/Common/Common/Mocap] select mh_lipsync_mapping_anim and PA_Metahuman_Lipsync.

4. RMB click to open context menu and select Asset Actions --> Migrate. Select "Content" folder of your project as a destination. Don't overwrite existing assets.

Done.
