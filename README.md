----Dot Hit Script----
--                --

while wait(0.1) do
	wait(0.1)
	
	--Variables--
	local Play = script.Parent.Parent
	local Character = Play.Character

	local Animacion = Character.Humanoid:LoadAnimation(script.Anim)
	--local Sonido = script.Sonido
	local DMG = Character.DMG.Value
	
	
	
if Character.Stun.Value == true then 

--VFX--
local hit = game.ReplicatedStorage.hit:Clone()
--Script--



		--UnMobility--
		Character.HumanoidRootPart.Anchored = true
			--Efectt--
			hit.Parent = game.Workspace
			hit.Position = Character.Torso.Position
			Animacion:Play()
			--Sonido:Play()
			
			wait(0.4)
			--Mobility And Stop Hit--
		Character.HumanoidRootPart.Anchored = false
		Animacion:Stop()
			hit:Destroy()
			--Sonido:Stop()
		
	end
end 
