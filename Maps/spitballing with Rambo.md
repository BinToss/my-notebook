- Replace Shields with fatigue
	- When Sprinting, fatigue is drained.
	- When fatigue is empty, the player is afflicted with a speed penalty (exhaustion)

- Extra HUD meters
	- Armor meter
	- HS functions
		- Toggleable (view)
		- Write to meter's values (current, max)
```cs
Class customMeter {
	public:
		short meterCurrent, meterMax;
}
```

- More realistic iron sights and scopes
	- Tilted weapon model (via animation?)