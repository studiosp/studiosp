
----Dot Hit Script----
--                --
--Variables--
     local Character = game.Player.LocalPlayer.Character
   local Play = game.Player.LocalPlayer
   local Animacion = Play.Character(script.Anim)
    local Sonido = script.Sonido
    local DMG = script.Parent.Dmg.Value
       --VFX--
         local hit = game.Workspace.hit:Clone()
       --Script--
      while wait(0.1) do
    if Character.Stun.Value == true then 
   Sonido:Play()
   --UnMobility--
   Character.HumanoidRootaPart.Anchored = true
  if Character.HumanoidRootPart.Anchored == true then
   --Efectt--
   hit.Parent = game.Workspace
   hit.Position = Character.Torso.Position
  Animacion:Play()
  Character.Humanoid:TakeDamage(DMG)
 wait(0.3)
 --Mobility And Stop Hit--
   Character.HumanoidRootaPart.Anchored = false
  Animacion:Stop()
  hit:Destroy()
  Sonido:Stop()
     end
  end
end 
