# MetahumVisemeCurves

This is simple Pose Asset with visemes for Epic's MetaHuman face skeleton. I used it for my Lip-Sync plugin.

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

1. Import MetaHuman character to your UE4/UE5 project.

2. Open MetahumVisemeCurves project.

3. In Content Browser under [Content/MetaHumans/Common/Common/Mocap] select mh_lipsync_mapping_anim and PA_Metahuman_Lipsync.

4. RMB click to open context menu and select Asset Actions --> Migrate. Select "Content" folder of your project as a destination. Don't overwrite existing assets.

Done.

## Note

If head moves down-up-forwad-back with the pose asset applied, open *Face_Archetype_Skeleton* and in its bones hierarchy change translation retargeting option for all bones except root and pelvis to "Skeleton".

## Note for Ynnk Voice Lip-Sync 

For owners of my plugin ([Ynnk Voice Lip-Sync](https://www.unrealengine.com/marketplace/en-US/product/ynnk-voice-lipsync)): you don't need this Pose Asset anymore. Go to menu Windows --> Visems Pose Asset Builder. In the dialog window select your face mesh (*[MetaHumanName]_FaceMesh* or default *Face_Archetype*), select ArKit mapping asset (*mh_arkit_mapping_pose*) and then click "Generate". It creates pose asset in the same folder with skeletal mesh. Then use it instead of PA_Metahuman_Lipsync. And make sure beforehand that mh_arkit_mapping_pose [isn't broken](https://forums.unrealengine.com/t/live-link-facial-animation-deformed-after-new-metahuman-release/578853/19).

AnimationTargets for this generated pose asset are a bit different:

((YV_KG, (Targets=("LS_G"))),(YV_BMP, (Targets=("LS_BMP"))),(YV_DSTL, (Targets=("LS_DST"))),(YV_Oh, (Targets=("LS_O"))),(YV_WU, (Targets=("LS_Uw"))),(YV_FV, (Targets=("LS_VF"))),(YV_Ee, (Targets=("LS_Eh"))),(YV_R, (Targets=("LS_R"))),(YV_ChShZh, (Targets=("LS_SH"))),(YV_N, (Targets=("LS_N"))),(YV_Ih, (Targets=("LS_Ih"))),(YV_OtherConsonant, (Targets=("LS_DST"))),(YV_OtherVowel, (Targets=("LS_Eh"))),(YV_Ah, (Targets=("LS_Aa"))))

Remember, neither PA_Metahuman_Lipsync or this generated asset is perfect. They're ok for start, but I'm sure it's possible to create better visemes for MetaHuman with proper efforts.
