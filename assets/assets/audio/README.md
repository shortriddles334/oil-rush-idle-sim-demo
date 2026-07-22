# Placeholder SFX

These `.wav` files are procedurally generated placeholder tones (simple sine
sweeps, chimes, and noise bursts), not real sound design. They exist so the
game has *some* audio feedback wired up end-to-end (see `lib/game/sfx.dart`)
without depending on external assets.

Swap them for real SFX whenever you have some - same filenames, same folder,
nothing else needs to change:

- `buy.wav` - shop purchase / package collected
- `drone_shot.wav` - drone fires
- `enemy_death.wav` - enemy killed
- `rig_damage.wav` - rig takes contact damage
- `victory.wav` - wave cleared
- `war_alert.wav` - war banner triggers
- `button_tap.wav` - generic UI button press (every button in the app)
- `achievement_unlock.wav` - an achievement is unlocked (`GameState.checkAchievements()`)
- `boss_pulse.wav` - boss's ranged pulse attack charge-up telegraph, fires
  0.6s before the pulse lands (`EnemyComponent.onPulseCharge`)
- `boss_defeat.wav` - boss enemy killed, replaces `enemy_death.wav` for that
  case (`OilRushGame`'s `onDied` callback)

`music/` holds the background loops generated locally via ComfyUI + ACE-Step
1.5 (see `AUDIO_GENERATION_PLAN.md`): `bgm_main_loop.mp3` (idle economy loop),
`bgm_war.mp3` (combat loop), `bgm_victory.mp3` (short victory sting).

Good free sources for real SFX: freesound.org (CC-licensed) or Kenney.nl's
audio packs (public domain, game-jam friendly).
