## v0.39.0 (2026-07-11)

### Feat

- **texture**: linear-light fp16 2D chain, W3C blend + composite, layer blend modes

## v0.38.0 (2026-07-10)

### BREAKING CHANGE

- 18 node types are removed from the registry:
scene.GIHybrid, scene.GIProbes, scene.GICache, scene.GISdf,
scene.GIRayTrace, scene.GICascades, scene.GIDDGI, scene.RestirIndirect,
scene.RestirIbl, scene.LightProbe, scene.SkyLight, texture.HorizonAO,
texture.RayAO, texture.ReflectScreen, texture.ReflectRayTrace,
texture.Denoise, texture.MotionBlurSS, and the duplicate
texture.ShaderToy (texture.Shadertoy is unaffected). Patches carrying
these nodes load with a dropped-node warning; none ever produced output.

### Feat

- delete 18 do-nothing nodes and fence the 3 that cannot draw (#170)

## v0.37.10 (2026-07-10)

### Fix

- **loop**: attest the open PR's head, not the branch the tree sits on
- **loop**: the reviewer could not read a diff
- **loop**: stop telling the executor to run a suite it cannot finish

## v0.37.9 (2026-07-09)

### Fix

- **render**: bloom reads its input same-frame, not one frame stale (#169)

## v0.37.8 (2026-07-08)

### Fix

- **color**: WhiteBalance neutral default is a true identity + honest FXAA docs

## v0.37.7 (2026-07-08)

### Fix

- **core**: run_shader output colorspace follows its primary input

## v0.37.6 (2026-07-08)

### Fix

- **particle**: cap RenderParticles2D draws to stop full-frame corruption (#166)

## v0.37.5 (2026-07-08)

### Fix

- **color**: stop ColorGrade3DLUT crashing the app on .cube load

## v0.37.4 (2026-07-07)

### Fix

- **render**: instanced draws survive off-origin framing (#164)

## v0.37.3 (2026-07-06)

### Fix

- **render**: keep skipped filters' cached textures alive across frames

## v0.37.2 (2026-07-06)

### Fix

- **render**: meshlet cone bounds via meshoptimizer + require CI on main (#162)
- **render**: meshlet cull tests real bounds from the real eye (#159)

## v0.37.1 (2026-07-03)

### Fix

- **render**: anisotropy shades in the mesh UV tangent frame (#158)

## v0.37.0 (2026-07-03)

### Feat

- **render**: KHR_texture_transform + second UV set (texCoord=1) (#157)

## v0.36.0 (2026-07-03)

### Feat

- **scene**: glTF KHR material extensions render as authored (#154)

## v0.35.0 (2026-06-14)

### Feat

- **render**: glTF animation playback — SkeletonPose plays authored clips, the sine pose is deleted (#153)

## v0.34.0 (2026-06-13)

### Feat

- **render**: apply glTF scene-node transform hierarchy on import (#152)

## v0.33.0 (2026-06-13)

### Feat

- **render**: per-texture glTF sampler states — DamagedHelmet renders canonically (#151)

## v0.32.1 (2026-06-12)

### Fix

- **render**: bindless texture array owns its views — ~100MB leaked per headless render (LUX-211) (#149)

## v0.32.0 (2026-06-12)

### Feat

- **render**: IBL chrome mirrors — UE4 reflection-capture mip schedule, coat mip, aniso metallic (#148)

## v0.31.0 (2026-06-12)

### Feat

- **render**: sorted transmissive pass — real see-through glass (LUX-175) (#147)

## v0.30.0 (2026-06-12)

### Feat

- **render**: bent-normal aniso IBL; BSDF doc-truth gate; honest docs (#146)

## v0.29.0 (2026-06-12)

### Feat

- **render**: BSDF feature_flags reach the GPU; seven lobes come alive (#145)

## v0.28.0 (2026-06-12)

### Feat

- **render**: wire Kaplanyan specular AA into both mesh shaders (#144)

## v0.27.0 (2026-06-12)

### Feat

- **render**: expose scene temporal upscaler; texture.Upscale honest (#143)

## v0.26.0 (2026-06-12)

### Feat

- **render**: TAA consumes gbuffer motion vectors; default on (#142)

## v0.25.0 (2026-06-12)

### Feat

- **render**: PCSS distance-dependent penumbra; the shadow_filter pin goes live (LUX-169) (#141)

## v0.24.2 (2026-06-12)

### Refactor

- **render**: delete the parked VSM stack — finish-or-delete resolved as delete (LUX-168) (#140)

## v0.24.1 (2026-06-11)

### Perf

- **render**: radiance cache samples 16 lights per ray hit — 1000_lights 25→4 ms/frame (#139)

## v0.24.0 (2026-06-11)

### Feat

- **render**: un-fake area + IES lights — canonical LTC port + profile sampling (LUX-166) (#138)

## v0.23.0 (2026-06-11)

### Feat

- **render**: omni point cube + spot shadow views; depth compare in metres (LUX-165) (#136)

### Fix

- **render**: update shadow orchestrator bench for LUX-165 ShadowEmitInputs (#137)

## v0.22.0 (2026-06-11)

### Feat

- **render**: cascade caster coverage + 48-direction sun sweep gate; loader rejects unknown pins; GI plugin registered (#135)

## v0.21.0 (2026-06-11)

### Feat

- **render**: water transmission + Jacobian caustics + flow advection; warn-once drops deleted (#134)

## v0.20.0 (2026-06-11)

### Feat

- **render**: Tessendorf FFT water for real — spectrum, butterflies, displaced surface (#133)

## v0.19.0 (2026-06-11)

### Feat

- **render**: sky-apply pass renders the Hillaire LUTs for real (#132)

## v0.18.0 (2026-06-11)

### Feat

- **render**: volumetric cloud trace + temporal denoise + depth-masked composite (#131)

## v0.17.0 (2026-06-11)

### Feat

- **render**: depth-aware volumetric fog composite; clear-color facade deleted (#130)

## v0.16.3 (2026-06-11)

### Fix

- **render**: fog inject + scatter dispatch for real; fake telemetry deleted (#129)

## v0.16.2 (2026-06-11)

### Fix

- **app**: CLI hardening — unknown flags never launch a window; dumps honor patch size (#128)

## v0.16.1 (2026-06-11)

### Fix

- **render**: readback contract — timeout is an error, short buffers rejected, warmup drains (#127)

## v0.16.0 (2026-06-11)

### Feat

- **core**: explicit active-output model — deterministic, visible, inert to unwired sinks (#126)

## v0.15.4 (2026-06-10)

### Fix

- **render**: windowed display shows per-frame GPU content; recycle transients (#125)

## v0.15.3 (2026-06-10)

### Fix

- **app**: restore Space=add-node and Tab=fuzzy-search; cue transport scopes to its panel (#124)

## v0.15.2 (2026-06-10)

### Fix

- **build**: restore the lux-render bench file that leaked out of this branch

## v0.15.1 (2026-06-10)

### Fix

- **app**: wall-clock test budgets become CI-aware; nextest reports all failures
- **app**: implement the documented runner-drift relax in the lockdown gate

## v0.15.0 (2026-06-10)

### Feat

- **render**: directional SH-L1 global illumination
- **app**: open a .lux patch from the CLI in the windowed app
- **render**: world-space single-bounce irradiance cache (first visible GI)

### Fix

- **app**: strengthen red_wall_bounce GI demo (wall flush, +light)
- **render**: guard GPU profiler against re-mapping an in-flight slot
- **render**: denoise the radiance cache (64 rays + spatial diffusion)
- **app**: rewrite stale red_wall_bounce GI demo + add regression test
- **render**: request bindless features on the windowed device so 3D renders

### Refactor

- **render**: carve radiance_cache.rs into a directory module

## v0.14.0 (2026-06-04)

### Feat

- **render**: add gbuffer/visibility prepass to Render3D framegraph (LUX-129)

## v0.13.0 (2026-06-04)

### Feat

- **scene**: route glTF textures so imported models render textured (LUX-127)

## v0.12.1 (2026-06-04)

### Refactor

- **render**: carve execute.rs arm bodies into texop_dispatch (LUX-25)

## v0.12.0 (2026-06-03)

### Feat

- **render**: run ACES 2.0 DRT as OCIO's GPU algorithm ported to WGSL (LUX-119)
- **render**: unify plugin tonemap onto lux::tonemap + 3D-LUT host binding
- **core**: reserve system-texture sentinel handles (LUX-18)
- **render**: route Render3D tonemap through lux::tonemap (LUX-18)
- **render**: engine-owned AgX/Tony 3D-LUT slabs for lux::tonemap (LUX-18)

### Fix

- **render**: extend ACES-2 LUT to EV[-12,7] + address review findings (LUX-119)
- **render**: bake real ACES 2.0 DRT into a LUT; delete the wrong hand-fit (LUX-119)
- **render**: external-reference tonemap gate + fix AgX/Tony bakes from real LUTs (LUX-115)
- **render**: scope shader compose hard-error to engine-internal shaders

## v0.11.0 (2026-05-29)

### BREAKING CHANGE

- adapters below Vulkan 1.2 / D3D12 / Metal 2 / WebGPU
2.0 (no `TEXTURE_BINDING_ARRAY` family) can no longer render 3D — there
is no legacy fallback. This is the LUX-77e adapter-floor decision.
- `lux_app::build_registry_v2` and
`lux_app::assert_registry_parity` are removed. Callers that were
asserting parity between the hand-rolled and inventory-driven paths
must drop the comparison — there is only one path now.
- `lux_core::scene::DrawItem` is now an enum;
construction sites must use `DrawItem::Static(StaticDrawItem { ... })`
or `DrawItem::Skinned(SkinnedDrawItem { ... })`. The legacy
`SkinnedMesh.out: Mesh` and `SkinnedMesh.material: Material` outputs
are deleted; patches that wired them must rewire to
`SkinnedMesh.skinned_draw → RenderScene.skinned`. The
`skin_cpu_fallback` Cargo feature is gone.
- `lux_core::scene::DrawItem` is now an enum;
construction sites must use `DrawItem::Static(StaticDrawItem { ... })`
or `DrawItem::Skinned(SkinnedDrawItem { ... })`. The legacy
`SkinnedMesh.out: Mesh` and `SkinnedMesh.material: Material` outputs
are deleted; patches that wired them must rewire to
`SkinnedMesh.skinned_draw → RenderScene.skinned`. The
`skin_cpu_fallback` Cargo feature is gone.
- `lux_app::build_registry_v2` and
`lux_app::assert_registry_parity` are removed. Callers that were
asserting parity between the hand-rolled and inventory-driven paths
must drop the comparison — there is only one path now.
- lux_render::light_store::LightType gained a new Ies = 9
variant. Pattern matches on LightType that omit a wildcard arm need to
add Ies. The 8-slot LightBlock uniform and its bind group are deleted —
any plugin shader still binding @group(N).LightBlock must migrate to the
cluster-bin LightStore path documented in CLAUDE.md "Shadow Orchestrator
+ Cluster-Forward+ Invariants".
- ColorGrade3DLUT no longer no-ops. Patches that relied
on the old pass-through behaviour now actually grade their input — this
is the documented intent of the node and the merge gate.
- `TransientAllocator::acquire` and `::release` signatures
have changed. External implementors must:
  - return `Result<ResourceBinding, UnsupportedKind>` from `acquire`
  - take `(kind: &ResourceKind, binding: ResourceBinding)` on `release`
  - use `ResourceBinding::Texture { .. }` for texture-flavored kinds
    and `ResourceBinding::Buffer { .. }` for Buffer kinds
- any external test that depended on `detect_fn_decl`
or `detect_mod_decl` from this test crate's internals will break --
those helpers were never `pub` and there are no known external
consumers, but flagged for completeness.
- the live 3D render path produces pixel-exact-different
output vs. pre-WS-2. The differences are mathematically correct (energy-
preserving Kulla-Conty compensation vs. the old lost-energy UE4-2013
approximation). Pre-launch policy: no compatibility toggle.
- `scene.PbrMaterial` node has five new pins. Existing
patches keep working -- unconnected Texture pins default to INVALID,
which maps to `None` in the scene material. The render-layer 1×1
fallbacks land in Pass F.
- `.lux` files that reference `texture.ToneMap` will
fail to load. No migration shim -- pre-launch policy.
- downstream patches that expected Rec.601 luma output
from Sobel / FXAA / Threshold / Luma-Blur will see a subtle luminance
shift. Lux is pre-launch so no compatibility shim is offered; this is
the right default going forward.
- `FORMAT_VERSION` advances from "2.0" to "2.2";
files saved by this build declare version 2.2. Readers pinned to
the old string must update their gate. Plugin authors constructing
`ProjectFile` directly must now supply `presets`, `cues`, and
`tempo_bpm` (all three default-constructible).
- PinType::Any now accepts as source (previously only
accepted as destination). Plugins that relied on Any-source being
rejected at connect time must be updated. In practice no existing
plugin has Any-source pins.
- Plugins that relied on `TextureFormat::default()` or
`TextureDesc::default()` implicitly giving `Rgba8` must now opt in
explicitly via `TextureFormat::Rgba8` / `TextureDesc::rgba8(w, h)`.
The in-tree audit found zero call sites using the default form — the
flip is a forward-looking contract change, not a code-breaking one.
- every render pipeline that samples or writes
depth now expects reverse-Z (near → 1, far → 0, compare
GreaterEqual, clear 0.0). Custom plugins that draw into the
scene depth buffer must update accordingly.

### Feat

- **render**: GPU instancing in the bindless arm (LUX-85 B-7.2) (#61)
- **render**: map legacy Blinn-Phong onto unified PBR (LUX-85 B-7.1) (#59)
- **render**: real bindless material-texture-array population (LUX-103)
- **render**: wire bindless mesh path live arm on bindless-capable adapters (LUX-77c)
- **render**: add BindlessCullState scaffold + lazy construction on TextureEngine
- **core**: SceneDesc partition methods for static/skinned draws
- **render**: wire MeshData -> MeshletPool upload in populate_from_scene
- **render**: add bindless @group(0) builder + 7-of-7 orchestrator bundle
- **render**: MeshPool retains Arc<MeshData> on persistent uploads (LUX-97 / LUX-77c.1)
- **render**: bindless orchestrator bind-group plumbing (LUX-82 / LUX-77b)
- **render**: bindless orchestrator stand-up (LUX-81 / LUX-77a)
- **scene-3d**: skinning fraud closure — DrawItem enum + skin_cpu retirement + GPU consumption (LUX-4)
- **framegraph**: sentinel deletion via Buffer export — close WS-1 §1 boundary
- **render**: async-compute live flip — Caps plumbing + FrameEncoderSplit (LUX-79)
- **render**: WS-4 — meshlet cull gates, bindless production pipeline, lux::pbr adoption (#6)
- **render**: WS-3 — Shadow Orchestrator + Clustered Forward+ Live Path (#5)
- **render**: WS-2 — Live-Path PBR + Color Pipeline Unification (#3)
- **framegraph,render**: wire all 7 ResourceKind variants through bridge_route (STEP 01 rework S1-R2 + S1-R3)
- **consent**: add participant consent form for usability study
- **render**: bake 4-channel BRDF LUT on the live IBL path (WS-2 Pass G)
- **render**: route live mesh path through lux::pbr (WS-2 Pass E + F)
- **scene**: expand PbrMaterial node to full glTF 2.0 pin surface (WS-2 Pass D)
- **render,framegraph**: adversarial review round 2 — real fixes (not cosmetic)
- **render,framegraph**: adversarial review fixes — batch 2 (core blockers)
- **framegraph,render**: STEP 01 sub-commit 1.4 — cross-queue barrier routes to destination encoder
- **framegraph,render**: EncoderDispatch for per-pass queue routing
- **framegraph**: ResourceKind additive expansion (STEP 07)
- **app**: Space/J/K cue hotkeys routed through live_binding (adoption-sweep 1.10b)
- **app,live**: LiveState on ProjectDocument + cue panel mount (adoption-sweep 1.10a)
- **render,app**: texop_ms 5-bucket split + lux-profile schema 2 (adoption-sweep 1.4)
- **ui**: browser fuzzy search (adoption-sweep 1.15)
- **ui**: bind H to ZoomToFit + fit-to-viewport math (adoption-sweep 1.16)
- **ui**: adopt wire_motion + spring-pop celebration (adoption-sweep 1.6)
- **ui**: ship Inter + proper label metrics (adoption-sweep 1.8)
- **ui**: hover/select tween + panel shadow elevation (adoption-sweep 1.7)
- **app**: global panic hook + crash-snapshot (adoption-sweep 1.17)
- **live,app**: MasterClock ticks once per frame → FrameContext::beat (adoption-sweep 1.9)
- **scene-character**: SkinnedMeshNode dispatches GPU skinning (adoption-sweep 1.18c)
- **render**: wire GpuProfiler into live app (adoption-sweep 1.3)
- **scene**: route SceneDesc.light.shadow_desc → LightStore (adoption-sweep 1.19)
- **core**: EvalState::dirty_node_count + HUD wiring (adoption-sweep 1.5)
- **core**: .lux schema 2.2 — presets, cues, tempo_bpm (adoption-sweep 1.11)
- **render**: Wave-10 — meshlet Hi-Z consumer wiring closes the loop
- **scene-character**: SkinnedMesh.pose pin + patch rewire (P2-B v2 commit 1/4)
- **render,scene-light**: P1 GAP-2 IES upload helper + pool + shader sampling
- **render**: Wave-8 orchestrator — Jimenez bloom end-to-end via framegraph
- **render**: Wave 8 #4 VSM software rasteriser foundation (actual)
- **render**: Wave 8 #4 VSM software rasteriser foundation
- **render**: P1-C subgroup-accelerated cluster_bin + parity test + bench
- **render**: Wave 7 #4 TemporalUpscale — FSR3-equivalent compute stage
- **render**: Wave-7 orchestrator — Hi-Z build end-to-end via framegraph
- **render**: B4-bis VSM page-caching foundation
- **render**: GAP-1 shadow e2e pixel gates + scene-3d shadow dispatch orchestrator
- **export**: P6-A render_one_frame — wire OfflineVideoRenderNode to real scene pipeline
- **render**: P2-B closeout — SKINNED vertex fetch in scene_buffer_write.wgsl
- **render**: P1 §2.4 — framegraph_bridge helpers + 5 passes on QueueAffinity::Compute
- **ui**: re-author 6 welcome samples against namespaced registry
- **scene-character**: P2-F material-pin wiring on GltfMesh + SkinnedMesh
- **core**: add PinValue::Any(PayloadArc) generic side-channel variant
- **export**: P6-D AovExr node + Filament AOV EXR sidecar writer
- **render**: P3-A bindless mesh pipeline + tier probe + cache key
- **render**: P3-B bindless mesh shader + naga_oil compile gate
- **render**: P3-C DrawStore DrawData SSBO + flush_to_gpu + std430 lock
- **render,scene-light**: P1 GAP-1 shadow framegraph wiring + 4 GPU validation tests
- **export**: P6-B ffmpeg-next mux + HDR10 PQ NV12 path
- **render**: P3 prereq GAP-3 — rewire render_3d.rs to scene-buffer P15 raster path
- **scene-primitives**: add RingTransforms3D + washer-ring sample
- **render**: P2-B compute skinning dispatch + framegraph wiring
- **ui,app**: P5-B first-wire celebration — spring-pop + chime + toast
- **render,live**: P1 GAP-4 HDR10 real swapchain reconfigure + ΔE round-trip gate
- **scene,render**: wire FogData + WaterData + FlowData + CausticsData from graph to renderer
- **onboarding**: capability-showcase samples — particle / SDF / PBR / feedback / beat grid
- **scene,render**: wire SkyData + CloudData from graph to atmosphere + cloud pipelines
- **scene-env-vol**: publish typed payloads on SkyDome / CloudField / FogField / WaterSurface / RiverFlow / Caustics
- **core**: add SkyData/CloudData/FogData/WaterData/FlowData/CausticsData PinValue variants
- **app**: P0-A lux-profile runner binary
- **render**: P0-A finish — gpu_profiler timestamp helpers + atmosphere wrap-up
- **app**: P5-A cold-start + first-pixel gates + deferral chip
- **export**: P6-A OfflineVideoRender node scaffold + offline EncoderMode
- **app**: P5-A cold-start + first-pixel gates + Shadertoy corpus + deferral chip
- **core**: P6-C FrameContext::with_offline_clock + rand::thread_rng lockdown (actual)
- **core**: P6-C FrameContext::with_offline_clock + rand::thread_rng lockdown
- **render**: P2-A skinning.wgsl compute + SKINNED MV branch
- **scene-character**: P2-D SkeletonPose + MorphTargets nodes
- Add closeout plans for P4 DDGI decision, P5 onboarding foundation, and P6 export
- **ui**: 3.7 UI — Ctrl+G wrap + breadcrumb bar (stub)
- **core**: 3.7 — SubpatchNode + SubpatchIn/Out data model + wrap()
- **scene-character**: 2.17 part 1 — glTF 2.0 import + GltfMesh + SkinnedMesh (CPU)
- **app,live**: G1-D — wire MultiWindowFleet + HdrLiveToggle + EncoderQueue into PresentationLayer
- **core**: PinValue::eq_cheap for O(1) spread-safe equality
- **core**: compute_levels — group ord values into par_iter-safe buckets
- **core**: Pearce-Kelly ord table + pk_delta algorithm
- **app**: EditorAction enum + drain pipeline
- **core**: SpreadValue columnar enum + 8 typed primitive variants
- **core**: ProcessContext::input_pin zero-alloc PinId overload
- **macro**: PinId + pins! macro codegens pub const PIN_FOO constants
- **core**: arena.rs — slotmap NodeId + NodeSlot struct (audit 1.1)
- **dependencies**: add lux-mapping package and update dependencies in Cargo.lock refactor(app): simplify display_name retrieval in LuxApp refactor(tests): improve readability of conditional checks in phase2_3d_family_goldens tests refactor(lux-live): streamline pub use statements in lib.rs refactor(pipelines): consolidate PipelineKey creation in denoise and restir pipelines refactor(pipelines): enhance readability of function calls in upscale.rs refactor(tests): format assertions for clarity in upscale_node_registration tests refactor(horizon_ao): tidy output_doc formatting in HorizonAoNode refactor(glsl_translate): improve readability of GLSL to WGSL translation functions refactor(shadertoy_node): clean up input and output documentation in ShadertoyNode
- **ui**: mapping_gizmo.rs — canvas gizmos for CornerPinWarp / ProjectionMesh / EdgeBlend
- **mapping**: lux-mapping plugin crate — CornerPinWarp, ProjectionMesh, EdgeBlend
- **texture-analyze**: D2 Kornia-class image analysis library (18 nodes)
- **app,texture-screen-space**: register lux-texture-screen-space + rename display names to identifier-form
- **live**: encode_queue.rs — dedicated encoder thread + 3-frame Rgba16F ring + hw-session probe
- **render**: denoise.rs orchestrator (P28) + pipelines/denoise.rs
- **render**: restir_indirect.rs orchestrator (P26)
- **render**: restir_direct.rs orchestrator (P25) + wire preserved WGSL
- **live**: multi_window.rs — WindowShell fleet + 16-cap + 50% VRAM enforcement
- **render,scene-gi,texture-screen-space**: B7 WIP — ReSTIR + Denoise shaders + lux-texture-screen-space crate (unreferenced)
- **ui**: status_bar.rs + pub mod decl (F2 follow-up)
- **live,core,ui,app**: F2 — PerfGuard 8-step ladder + hitch capture + crash sandbox + BeatContext on FrameContext
- **render,scene-material**: pbr.wgsl evaluate_shade routes every FeatureBits variant to its lobe (BLOCKER #1 §3)
- **scene-material**: wire MaterialGraph BSDF compile + #[lux_node] migration (BLOCKER #1 + #2)
- **render,texture-shader**: D1 HDR Vello + Shadertoy URL paste + HDR feedback
- **render**: B8 Upscale (Temporal+FSR3+MotionBlur) + HDR tonemap branches
- **ui**: cue_panel.rs — List/Timeline + Go button + Space shortcut
- **live**: device_manager.rs — DeviceEvent broadcaster (hooks only)
- **live**: crash_sandbox.rs — shader + eval + device-lost isolation
- **live**: async_warmer.rs — background pipeline compile + persistent cache at ~/.cache/lux/
- **live**: beat_context.rs — MasterClock priority chain + IIR phase filter + rising-edge emitters
- **live**: transition_machine.rs — Stable/Transitioning/WarmingOnly + dual-pipeline Crossfade
- **live**: CueList + Transition enum + CueTrigger + CueMode
- **live**: PresetSnapshot with Arc-shared SceneDesc + thumbnail persistence
- **live**: new lux-live crate + module scaffolding
- **scene-environment-vol**: FogField / CloudField / WaterSurface / RiverFlow / Caustics nodes
- **render**: fog_field + cloud_field + water_surface + pipelines — BY/BZ/BW orchestrators
- **render**: shaders/volume + shaders/wave WGSL — volumetric + ocean passes
- **scene-gi**: new plugin crate + GIHybrid/Probes/Cache/Sdf/RayTrace/Cascades/DDGI + RestirIndirect/Ibl + LightProbe + SkyLight
- **core**: SceneDesc Vec-pluralized fog/cloud/water_surface fields
- **render**: pipelines/hybrid_gi.rs — per-mode + dispatcher via PipelineCache
- **render**: shaders/modules/probe_field.wgsl + shaders/gi/* — unified trace_ray
- **render**: rt_accel.rs — TLAS/BLAS builder, feature-gated hw_rt (P24)
- **render**: sdf_trace.rs — per-mesh sparse SDF brick + sphere-tree (P23)
- **render**: radiance_cache.rs — 8K² world-space radiosity atlas (P22)
- **render**: surface_probes.rs — 1/8-res screen-aligned probe grid (P20-P21)
- **render**: framegraph wire P17 strand_raster
- **render**: FIBER case in pbr.wgsl evaluate_shade dispatch
- **scene-character**: new plugin crate + Strands + FiberMaterial ("Hair / Fur Material")
- **render**: pipelines/strand.rs — line + cards pipelines via PipelineCache
- **render**: shaders/scene/strand_cards.wgsl — card-mesh LOD fallback
- **render**: use PrismComposer for P28b/P29 shader compile
- **render**: framegraph wire P16 splat sort + P32 raster + BarrierPlan
- **scene-light**: DirectionalLight/PointLight/SpotLight gain shadow_storage × shadow_filter × contact_shadows × ies_profile pins
- **scene-exotic-geo**: new plugin crate + GaussianSplatField node
- **render**: splat_field.rs — .splat loader + .spz deferral stub
- **core**: SceneDesc.splat_sets field + SplatFieldSet struct
- **render**: B3 wiring — framegraph P15/P28b/P29 + BarrierPlan batching
- **render**: pipelines/shadow.rs — VSM + CSM pipelines via PipelineCache
- **render**: shaders/scene/depth_pass.wgsl — shared meshlet depth prepass (P13)
- **render**: integrate B3/B4/BU/BV partial modules into lib + pipelines + hot-path scan
- **render**: BV partial — strand_raster.wgsl (quota-interrupted)
- **render**: BU partial — Gaussian splat sort + EWA raster shaders (quota-interrupted)
- **render**: B4 partial — Virtual Shadow Maps + CSM fallback (quota-interrupted)
- **render**: B3 partial — scene-buffer + shade-classify + deferred shade (quota-interrupted)
- **render**: shaders/modules/fiber.wgsl — Marschner R/TT/TRT + d'Eon multi-scatter + glint
- **render**: strand_pool.rs — 100K × 32-seg GPU pool
- **render**: shaders/post/autoexposure_histogram.wgsl (Phase 2 C2)
- **texture-filter**: Tonemap, ColorGrade3DLUT, OklabGrade, OklchHueShift, AutoExposure, WhiteBalance (Phase 2 C2)
- **assets**: bundle agx_48.cube + tony_48.cube (Phase 2 C2)
- **render**: lut3d .cube parser + AgX/Tony bakers (Phase 2 C2)
- **render**: unified tonemap.wgsl + modules/oklab.wgsl (Phase 2 C2)
- **ui**: drop_handler — file-extension → loader-node classifier
- **scene-environment-vol**: SkyDome node with sun/moon/stars + SkyData pin
- **render**: pipelines/atmosphere.rs — Hillaire 2020 LUT bake + dirty tracking
- **ui**: implicit_wire policy — auto-wire 2D / 3D / audio chains
- **render**: B5 cluster light binning + LTC area lights — infra landing
- **ui**: tag-first browser search — trigram pre-filter + multi-field scoring
- **ui**: welcome gallery — 3×2 curated sample grid with hover lift
- **app**: six hello_*.lux welcome samples bundled via include_bytes!
- **core**: onboarding module — starter palette + display names + popular + shadertoy URL
- **render**: shaders/modules/brdf.wgsl + multiscatter.wgsl + pbr.wgsl
- **render**: 4-channel BRDF LUT + 3D anisotropic Ess LUT
- **scene-material**: MaterialGraph + BSDF lobes + OpenPBR 2024 + Fdez-Agüera MS
- **ui**: hud.rs — 120 FPS tripwire colours + headroom percentage
- **render**: modules/color.wgsl — OETF/EOTF/PQ/HLG/CAT16 primitives
- **render**: modules/velocity.wgsl — motion-vector pack + compute
- **render**: modules/normal_aa.wgsl — Toksvig filter for shading-normal AA
- **render**: modules/noise.wgsl — value/gradient/Worley/FBM/curl/Simplex/domain-warp
- **ui**: cursor.rs — 10 named states with egui fallback + overlay hint
- **render**: modules/sampling.wgsl — Halton/Hammersley/Poisson/pcg/ign/blue-noise
- **ui**: typography.rs — 8 TypeRoles mapping Inter + JB Mono sizes
- **render**: modules/camera.wgsl — CameraUniforms binding + physical exposure + camera_ray
- **render**: modules/common.wgsl — reverse-Z helpers, octahedral, luma, safe ops
- **ui**: wire_motion.rs — 8-state machine with beat-sync + reduce-motion
- **render**: meshlet task-shader cull + Hi-Z build + indirect draw (B2 P07/P08/P13/P15)
- **render**: meshlet_pool with 1M-meshlet GPU SSBO + cone/sphere bounds + LOD
- **ui**: theme.rs — OkLch family stripes + HDR preview + light theme
- **ui**: motion.rs durations / easings / Springs / Pulse + beat sync
- **render**: reverse-Z projection + depth-compare GreaterEqual + clear 0.0
- **render**: bind_group_cache keyed on layout + resource hashes (B9.4)
- **render**: barrier_plan batching — one transition_resources per pass edge (B9.3)
- **render**: draw store with 2-ring + separate cluster mask SSBO (B9.2)
- **render**: bindless material table with dirty-range coalesce + T2/T3 atlas fallback (B9.1)
- **app**: F8 HUD per-pass mode with rolling p50/p95 + Tab cycling
- **render**: Phase 2a Wave 2 — GPU tier probe, HDR output, gpu_profiler, pipeline_cache
- **app**: family-golden harness with SSIM / ΔE76 / PSNR thresholds + 5 Phase 1 baselines
- **core**: Phase 1 → Phase 2 JSON migrator
- **core**: Phase 2a foundations — canonical interfaces + #[lux_node] macro

### Fix

- **render**: make no_hot_path_sync blocking audit directory-aware (PR-M) (#89)
- **bench**: correct realhw_frame_budget patch paths (#71)
- **scene**: mark SkinnedMesh rest mesh persistent so it rasterizes (LUX-I-110) (#65)
- **render**: size cluster light-index pool for worst case (LUX-108) (#63)
- **render**: activate bindless arm + close 4 rendering bugs (LUX-85 B-6) (#58)
- **core**: MaterialGpu CPU/GPU std430 layout drift (LUX-85 B-2 prep)
- **render**: close LUX-103 B-1 implicit recycle hole (LUX-104)
- **render**: close 3 of 5 architect-flagged LUX-103 soft concerns + B-1 partial fix
- **render**: bindless-arm shadow pre-raster fixes mixed-caster artifact (LUX-77c soft concern C-5)
- **render**: close LUX-77c blockers caught by adversarial review
- **render**: graceful skip on missing pipeline resources, not panic
- **framegraph,render**: STEP 07 round-5 adversarial fixes
- **framegraph,render**: STEP 07 round-4 adversarial fixes
- **framegraph,render**: STEP 07 round-3 adversarial fixes
- **render**: Arc-stable BindGroupCache keys for pooled uniform buffers
- **app,render**: integrate adoption-sweep — storage-buffer limit + baseline bump + docs path
- **onboarding**: welcome 11/11 dispatch + recents + first-wire persistence (adoption-sweep 1.12-1.14)
- **export**: P6-B libx265 GPL guard — BSD-first HEVC priority
- **build**: workspace cargo check green — wgpu 29 + SceneDesc drift cleanup
- **render**: rename scene_skinning `gen` identifier → `generation` (Rust 2024 keyword)
- **app**: P0-A — hook scene render path + add total_gpu_ms summary
- **render**: edge_blend.wgsl S-curve for luminance invariance
- **core**: flip TextureFormat::default() to Rgba16Float (architect HIGH #6)
- **core**: deprecate FromPinValue<Material> deep-clone in favour of Arc<Material>
- **render**: integrate B8 upscale + BY/BZ/BW SceneDesc Vec fields + misc
- **scene-material**: restore BSDFAnisotropic see_also → FiberMaterial (now registered)
- **render**: debug + fix shadow_vsm page-allocator fill-to-cap + cache-hit-rate tests
- **scene-material**: drop see_also pointers to unimplemented FiberMaterial/FabricMaterial/SubsurfaceMaterial nodes
- **app**: wire WelcomeChoice::OpenRecent/ReferenceGallery + NodeIndexEntry new fields
- **ui**: replace label.len()*6.0 kerning with derived mono glyph advance
- **texture**: invert linearize_depth + sky-skip for reverse-Z in ssao / dof / visualize_depth

### Refactor

- **render**: delete dormant deferred-shade chain (LUX-17) (#90)
- **export-video**: carve 3 export-video god-files (LUX-16 PR-K) (#87)
- **plugins/scene**: carve 5 scene plugin god-files (LUX-16 PR-J) (#86)
- carve last 2 LUX-16 god-files — pin_value + interface_drift (PR-I) (#85)
- **render**: carve 5 lux-render bench/test god-files (LUX-16 PR-H) (#84)
- **live**: carve 4 lux-live god-files (LUX-16 PR-G) (#83)
- **framegraph**: carve 3 lux-framegraph god-files (LUX-16 PR-F) (#82)
- **app**: carve 6 lux-app god-files (LUX-16 PR-E) (#81)
- **ui**: carve 9 lux-ui god-files (LUX-16 PR-D) (#80)
- **render**: carve 6 final lux-render god-files (LUX-16 PR-C4) (#79)
- **render**: carve 6 backend/pipeline god-files (LUX-16 PR-C3) (#78)
- **render**: carve 6 scene/pipeline god-files + fix hot-path audit (LUX-16 PR-C2) (#77)
- **render**: carve 4 bindless god-files + decompose dispatch_render3d_bindless_arm (LUX-16 PR-C1) (#76)
- **core**: carve 8 lux-core mid-size god-files into modules (LUX-16 PR-B) (#75)
- **core**: carve pin.rs + eval.rs god-files into focused modules (LUX-16 PR-A3) (#74)
- **core**: carve graph.rs god-file into focused modules (LUX-16 PR-A2) (#73)
- **core**: carve context.rs god-file into focused modules (LUX-16 PR-A1) (#72)
- **render**: carve framegraph_bridge.rs god-file into focused modules (LUX-15) (#70)
- **render**: drop stale "fall back to legacy" text in bindless dispatch
- **render**: delete the legacy render_3d::execute renderer (LUX-85 B-5) (#62)
- **render**: delete dispatch_legacy_fallback (LUX-85 B-4.5 part 1) (#56)
- **render**: DEPTH_ONLY × IS_SKINNED skinned-shadow pipeline (LUX-85 B-4.4) (#55)
- **render**: skinned bindless multi-draw + delete legacy skinned post-pass (LUX-85 B-4.3) (#54)
- **render**: skin compute → unified deformed scatter (LUX-85 B-4.2) (#53)
- **render**: UnifiedDeformedBuffer allocator on BindlessState (LUX-85 B-4.1) (#52)
- **render**: BindlessSkinnedMeshPipeline + IS_SKINNED permutation (LUX-85 B-4.0) (#50)
- **render**: bindless CSM cascade cull + raster (LUX-85 B-3.2) (#49)
- **render**: BindlessShadowPipeline + DEPTH_ONLY permutation (LUX-85 B-3.1) (#48)
- **render**: multi-cascade MeshletIndirectOutput slots (LUX-85 B-3.0) (#47)
- **render**: frame-0 no-Hi-Z bindless dispatch via depth stub (LUX-85 B-2) (#46)
- **render**: bindless arm vertex-pulling redesign (LUX-106) (#45)
- hoist plugin-cross payloads to lux-core (LUX-10) (#43)
- **render**: close WS-1 §6 LOC budget on engine/*.rs (LUX-102 + LUX-103 C-1)
- **render**: bundle bindless state to type-pin "all four or none" invariant (LUX-104 C-2)
- **render**: single source of truth for shadow caster slot scan (LUX-77c soft concern C-3)
- **render**: carve bindless arm + lazy-build out of render3d_dispatch (WS-1 §6 budget)
- **app**: collapse build_registry to inventory walk (LUX-76)
- **plugins**: #[lux_node] migration — Math + Logic family (LUX-6.1)
- **plugins**: #[lux_node] migration — Animation family (LUX-6.2)
- **render**: drop framegraph_chain raw-pointer fallback view
- **ui**: drop WelcomeState::Template — sample gallery is the only mode
- **core**: delete lux-core::migration module — strict-equality version gate
- **core**: drop Material deep-clone shim — Arc<Material> wire form only
- **plugins**: #[lux_node] migration — Spread family (LUX-6.3)
- **plugins**: #[lux_node] migration -- Shape + SDF + Particle (LUX-6.5)
- **plugins**: #[lux_node] migration — Texture filter + source (LUX-6.6)
- **plugins**: #[lux_node] migration — Texture rest + Scene primitives/transform (LUX-6.7)
- **plugins**: #[lux_node] migration — Scene non-shading + Export (LUX-6.8)
- **plugins**: #[lux_node] migration — IO + Color + String + Mapping (LUX-6.4)
- **framegraph,render**: STEP 01 rework S1-R7 -- Sev-2 quality cleanups
- **test**: replace no_hot_path_sync brace-counter with syn AST walker (STEP 01 rework S1-R1)
- **render**: split modules/pbr.wgsl into params-form core + bindless adapter (WS-2 Pass C)
- **color**: delete legacy plugin tone_map.wgsl / ToneMap node (WS-2 Pass B)
- **color**: flip plugin shaders from Rec.601 to Rec.709 luma (WS-2 Pass A)
- **render,framegraph**: adversarial review fixes — batch 3 (refinement)
- **render,framegraph**: adversarial review fixes — batch 1 (easy wins)
- **render**: STEP 01 sub-commit 1.6b — texture_engine.rs carve-out complete
- **render**: STEP 01 sub-commit 1.6a — texture_engine.rs carve-out (free fns)
- **render**: delete pointer-keyed BindResourceRef::Buffer variants
- **render**: retire LUX_BARRIER_PLAN env flag — explicit barriers always on
- **core,app**: registry from inventory — #[lux_node] factory + build_registry_v2 (adoption-sweep 1.20)
- **export**: P6-D AovExr consumes PinValue::Any instead of FlowData
- **core**: EvalState::evaluate uses rayon per-level par_iter
- **core**: Graph::connect uses Pearce-Kelly, deletes full-Kahn call
- **app**: migrate #[cfg(test)] module to tests/ integration
- **app**: panels as free functions — export dialog + progress overlay
- **app**: extract FrameLoop (render passes + present + texture sync)
- **app**: extract EditorChrome (editor + welcome + cheatsheet + dialogs + caches + recent_files + prefs + search_index + sequence_export)
- **app**: extract PresentationLayer (render_state + egui_winit + output + texture_engine)
- **app**: extract ProjectDocument (graph + undo + path + dirty + autosave)
- **app**: extract FrameScheduler (timing + profiler + perf_guard + hitch)
- **app**: extract InputRouter (input_state + handlers + helpers)
- **core**: Spread(Vec<PinValue>) -> Spread(Arc<[PinValue]>) for O(1) wire clone
- **core**: eval+graph migrate to SlotMap arena + gen-counter dirty gate (audit 1.1 + 1.4)
- **core,pbr**: reconcile MaterialGpu 256B with spec via detail_occlusion + opacity_mask texture slots (architect HIGH #7)
- **texture-filter**: migrate 8 Phase-2 filter nodes to #[lux_node] (BLOCKER #2 part 5/5)
- **scene-exotic-geo**: migrate GaussianSplatField to #[lux_node] (BLOCKER #2 part 3/5)
- **scene-environment-vol**: migrate 6 sky/fog/cloud/water nodes to #[lux_node] (BLOCKER #2 part 2/5)
- **scene-light**: migrate 4 light nodes to #[lux_node] (BLOCKER #2 part 1/5)

### Perf

- **render**: unify Render3D onto one run_with_dispatch framegraph (LUX-14) (#69)
- **render**: lift BindGroupCache to TextureEngine hot-path sites (LUX-13) (#68)
- **render**: eliminate 3 per-frame SceneDesc clones on Render3D path (LUX-100)
- **render**: pre-build BindlessFallbackArrays slices + dedup sampler (LUX-77c soft concerns C-1, C-7)
- **render**: STEP 01 sub-commit 1.5 — scene_bloom BindGroupCache adoption
- **render**: O(1) pass-indexed BarrierPlan batch lookup
- **render**: BarrierPlan on post chain behind LUX_BARRIER_PLAN flag (adoption-sweep 1.2)
- **render**: BindGroupCache adoption across scene post chain (adoption-sweep 1.1)
- **core**: track actually-processed set for predecessor short-circuit
- **core**: clean-subtree free-pass + O(|delta|) wire transfer
- **core**: transfer_wire_data skips gen-bump when value unchanged
- **core**: graph_eval_no_string_alloc reports 1 alloc/frame on 1000-node pass
- **core**: gen_at_last_eval fast-path + always_dirty_ids sidecar
- **sdf**: lux-raymarch output_2d scratch-Vec on hot path (architect HIGH #9)

## v0.10.0 (2026-04-20)

### Feat

- **node**: LoadImage decodes .hdr + tags 8-bit as sRGB
- **node**: red error dot + tinted border for panicking nodes
- **ui**: route backward wires with extended lead-out + vertical lift
- **ui**: magnet-snap wire drag to nearest compatible pin
- **ui**: wire-drag search filters by pin type + auto-connects on pick
- **ui**: pin tooltips show defaults + ranges
- **ui**: fuzzy search indexes summary + tags, not just type names
- **ui**: menu bar + ? cheatsheet + empty-canvas CTA
- **ui**: welcome splash modal on first launch
- **app**: replace hardcoded triangle demo with Mouse → Circle sample
- **core**: add UserPrefs persistence to ~/.config/lux/prefs.json
- **ui**: add motion.rs — single source of truth for editor animation
- **app**: F8 frame-budget profiler HUD + tripwire logging

### Fix

- **node**: drop dead `ambient` pin from LambertMaterial
- **node**: naming hygiene — unify category separator, dedupe Mirror, hide stub Path
- **node**: close GPU texture leaks in texture-source + feedback
- **ui**: use egui default sans-serif for Proportional text

### Perf

- **node**: borrow input spreads by slice in read-only spread ops

## v0.9.0 (2026-04-20)

## v0.8.0 (2026-04-20)

## v0.7.0 (2026-04-20)

## v0.6.0 (2026-04-20)

## v0.5.0 (2026-04-20)

## v0.4.0 (2026-04-20)

## v0.3.0 (2026-04-20)

## v0.2.0 (2026-04-20)

## v0.10.0 (2026-04-20)

### Feat

- **node**: LoadImage decodes .hdr + tags 8-bit as sRGB
- **node**: red error dot + tinted border for panicking nodes
- **ui**: route backward wires with extended lead-out + vertical lift
- **ui**: magnet-snap wire drag to nearest compatible pin
- **ui**: wire-drag search filters by pin type + auto-connects on pick
- **ui**: pin tooltips show defaults + ranges
- **ui**: fuzzy search indexes summary + tags, not just type names
- **ui**: menu bar + ? cheatsheet + empty-canvas CTA
- **ui**: welcome splash modal on first launch
- **app**: replace hardcoded triangle demo with Mouse → Circle sample
- **core**: add UserPrefs persistence to ~/.config/lux/prefs.json
- **ui**: add motion.rs — single source of truth for editor animation
- **app**: F8 frame-budget profiler HUD + tripwire logging

### Fix

- **node**: drop dead `ambient` pin from LambertMaterial
- **node**: naming hygiene — unify category separator, dedupe Mirror, hide stub Path
- **node**: close GPU texture leaks in texture-source + feedback
- **ui**: use egui default sans-serif for Proportional text

### Perf

- **node**: borrow input spreads by slice in read-only spread ops

## v0.9.0 (2026-04-20)

## v0.8.0 (2026-04-20)

## v0.7.0 (2026-04-20)

## v0.6.0 (2026-04-20)

## v0.5.0 (2026-04-20)

## v0.4.0 (2026-04-20)

## v0.3.0 (2026-04-20)

## v0.9.0 (2026-04-20)

## v0.8.0 (2026-04-20)

## v0.7.0 (2026-04-20)

## v0.6.0 (2026-04-20)

## v0.5.0 (2026-04-20)

## v0.4.0 (2026-04-20)

## v0.3.0 (2026-04-20)

## v0.2.0 (2026-04-20)

## v0.1.0 (2026-04-20)

