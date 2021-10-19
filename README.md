----Dot Hit Script----
--                --
while wait(0.1) do
	
	
	--Variables--
	local Play = script.Parent.Parent
	local Character = Play.Character

	local Animacion = Character.Humanoid:LoadAnimation(script.Anim)
	local Sonido = script.Sonido
	local DMG = Character.DMG.Value
	
	
	
if Character.Stun.Value == true then 

--VFX--
local hit = game.ReplicatedStorage.hit:Clone()
--Script--



		--UnMobility--
		Character.HumanoidRootPart.Anchored = true
		--Efectt--
		wait(0.2)
			hit.Parent = game.Workspace
			hit.Position = Character.HumanoidRootPart.Position
			Animacion:Play()
			Sonido:Play()
		Character.Humanoid:TakeDamage(DMG)
			wait(0.7)
			--Mobility And Stop Hit--
		Character.HumanoidRootPart.Anchored = false
		Animacion:Stop()
			hit:Destroy()
			Sonido:Stop()
		wait(0.2)
	end
end 

