HumanDied = false
_G.ClickFling=false -- Set this to true if u want.


plr = game.Players.LocalPlayer
char=game.Players.LocalPlayer.Character
ct={}
te=table.insert

HumanDied=false

local mode = 0
local dancing = false

for i,v in next, game:GetService("Players").LocalPlayer.Character:GetDescendants() do
if v:IsA("BasePart") then 
te(ct,game:GetService("RunService").Heartbeat:connect(function()
pcall(function()
v.Velocity = Vector3.new(0,-30,0)
sethiddenproperty(game.Players.LocalPlayer,"MaximumSimulationRadius",math.huge)
sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",999999999)
game.Players.LocalPlayer.ReplicationFocus = workspace
end)
end))
end
end

function notify(t,tex,dur)
game.StarterGui:SetCore("SendNotification", {
    Title = t; 
    Text = tex; 
    Duration = dur or 5;
})
end

local srv= game:GetService("RunService")

fl=Instance.new('Folder',char);fl.Name='CWExtra'

char.Archivable = true
local reanim = char:Clone()
reanim.Name='NexoPD'

for i,v in next, reanim:GetDescendants() do
if v:IsA('BasePart') or v:IsA('Decal') then
v.Transparency = 1 
end 
end

--flinge = false

penis=5.65
plr.Character=nil
plr.Character=char
char.Humanoid.AutoRotate=false
char.Humanoid.WalkSpeed=0
char.Humanoid.JumpPower=0
char.Torso.Anchored = true
notify('Nexo','Reanimating...\nPlease wait '..penis..' seconds.')
wait(penis)
char.Torso.Anchored=false
notify('Nexo','Reanimated..')
char.Humanoid.Health=0
--reanim.Humanoid.AutoRotate=false
reanim.Animate.Disabled = true
reanim.Parent = fl
reanim.HumanoidRootPart.CFrame = char.HumanoidRootPart.CFrame*CFrame.new(0,5,0)

function create(part, parent, p, r)
Instance.new("Attachment",part)
Instance.new("AlignPosition",part)
Instance.new("AlignOrientation",part)
Instance.new("Attachment",parent)
part.Attachment.Name = part.Name
parent.Attachment.Name = part.Name
part.AlignPosition.Attachment0 = part[part.Name]
part.AlignOrientation.Attachment0 = part[part.Name]
part.AlignPosition.Attachment1 = parent[part.Name]
part.AlignOrientation.Attachment1 = parent[part.Name]
parent[part.Name].Position = p or Vector3.new()
part[part.Name].Orientation = r or Vector3.new()
part.AlignPosition.MaxForce = 999999999
part.AlignPosition.MaxVelocity = math.huge
part.AlignPosition.ReactionForceEnabled = false
part.AlignPosition.Responsiveness = math.huge
part.AlignOrientation.Responsiveness = math.huge
part.AlignPosition.RigidityEnabled = false
part.AlignOrientation.MaxTorque = 999999999
part.Massless=true
end

function Pos(part, parent, p)
Instance.new("Attachment",part)
Instance.new("AlignPosition",part)
Instance.new("Attachment",parent)
part.Attachment.Name = part.Name
parent.Attachment.Name = part.Name
part.AlignPosition.Attachment0 = part[part.Name]
--part.AlignOrientation.Attachment0 = part[part.Name]
part.AlignPosition.Attachment1 = parent[part.Name]
--part.AlignOrientation.Attachment1 = parent[part.Name]
parent[part.Name].Position = p or Vector3.new()
part.AlignPosition.MaxForce = 999999999
part.AlignPosition.MaxVelocity = math.huge
part.AlignPosition.ReactionForceEnabled = false
part.AlignPosition.Responsiveness = math.huge
--part.AlignOrientation.Responsiveness = math.huge
--part.AlignPosition.RigidityEnabled = false
--part.AlignOrientation.MaxTorque = 999999999
part.Massless=true
end

for i,part in next, char:GetDescendants() do
if part:IsA('BasePart') then
te(ct,srv.RenderStepped:Connect(function()
part.CanCollide=false
end))
end
end

for i,part in next, char:GetDescendants() do
if part:IsA('BasePart') then
te(ct,srv.Stepped:Connect(function()
part.CanCollide=false
end))
end
end

for i,part in next, reanim:GetDescendants() do
if part:IsA('BasePart') then
te(ct,srv.RenderStepped:Connect(function()
part.CanCollide=false
end))
end
end

for i,part in next, reanim:GetDescendants() do
if part:IsA('BasePart') then
te(ct,srv.Stepped:Connect(function()
part.CanCollide=false
end))
end
end

for i,v in next, char:GetDescendants() do
if v:IsA('Accessory') then
create(v.Handle,reanim[v.Name].Handle)
end
end

--Pos(fhrp,reanim['Torso'])
create(char['Head'],reanim['Head'])
create(char['Torso'],reanim['Torso'])
Pos(char['HumanoidRootPart'],reanim['Torso'],Vector3.new(0,0,0))
create(char['Right Arm'],reanim['Right Arm'])
create(char['Left Arm'],reanim['Left Arm'])
create(char['Right Leg'],reanim['Right Leg'])
create(char['Left Leg'],reanim['Left Leg'])

m = plr:GetMouse()

local LVecPart = Instance.new("Part", fl) LVecPart.CanCollide = false LVecPart.Transparency = 1

te(ct,srv.RenderStepped:Connect(function()
local lookVec = workspace.CurrentCamera.CFrame.lookVector
local Root = reanim["HumanoidRootPart"]
LVecPart.Position = Root.Position
LVecPart.CFrame = CFrame.new(LVecPart.Position, Vector3.new(lookVec.X * 10000, lookVec.Y, lookVec.Z * 10000))
end))

wdown=false
sdown=false
adown=false
ddown=false
spacedown=false

--reanim.HumanoidRootPart.RootJoint.Part0=nil

function flinger(p)
f=Instance.new('BodyAngularVelocity',p)
f.AngularVelocity = Vector3.new(9e9,9e9,9e9)
f.MaxTorque=Vector3.new(9e9,9e9,9e9)
end

flinger(char.HumanoidRootPart)

m=plr:GetMouse()

--char.HumanoidRootPart.Transparency = 0

bp=Instance.new('BodyPosition',char.HumanoidRootPart)
bp.P = 9e9
bp.D = 9e9
bp.MaxForce=Vector3.new(99999,99999,99999)

local click

te(ct,srv.Heartbeat:Connect(function()
if click == true then
bp.Position=m.Hit.p
char.HumanoidRootPart.Position=m.Hit.p
else
bp.Position=reanim.Torso.Position
char.HumanoidRootPart.Position=reanim.Torso.Position
end
end))

local Highlight = Instance.new("SelectionBox")
Highlight.Adornee = char.HumanoidRootPart
Highlight.LineThickness=0.05
Highlight.Color3 = Color3.fromRGB(30,255,30)
Highlight.Parent = char.HumanoidRootPart
Highlight.Name = "RAINBOW"

hrp = Highlight

spawn(function()
while true do
srv.Stepped:Wait()
if ded then break end
hrp.Color3 = Color3.new(255/255,0/255,0/255)
for i = 0,255,10 do
wait()
hrp.Color3 = Color3.new(255/255,i/255,0/255)
end
for i = 255,0,-10 do
wait()
hrp.Color3 = Color3.new(i/255,255/255,0/255)
end
for i = 0,255,10 do
wait()
hrp.Color3 = Color3.new(0/255,255/255,i/255)
end
for i = 255,0,-10 do
wait()
hrp.Color3 = Color3.new(0/255,i/255,255/255)
end
for i = 0,255,10 do
wait()
hrp.Color3 = Color3.new(i/255,0/255,255/255)
end
for i = 255,0,-10 do
wait()
hrp.Color3 = Color3.new(255/255,0/255,i/255)
end
end
end)

te(ct,m.Button1Down:Connect(function()
click=true
end))

te(ct,m.Button1Up:Connect(function()
click=false
end))

te(ct,m.KeyDown:Connect(function(e)
if e ==' ' then
spacedown=true end
if e =='w' then
wdown=true end
if e =='s' then
sdown=true end
if e =='a' then
adown=true end
if e =='d' then
ddown=true
end
end))

te(ct,m.KeyUp:Connect(function(e)
if e ==' ' then
spacedown=false end
if e =='w' then
wdown=false end
if e =='s' then
sdown=false end
if e =='a' then
adown=false end
if e =='d' then
ddown=false
end
end))

local function MoveClone(X,Y,Z)
LVecPart.CFrame = LVecPart.CFrame * CFrame.new(-X,Y,-Z)
reanim.Humanoid.WalkToPoint = LVecPart.Position
end

te(ct,srv.RenderStepped:Connect(function()
if wdown==true then
MoveClone(0,0,1e4) end
if sdown==true then
MoveClone(0,0,-1e4) end
if adown==true then
MoveClone(1e4,0,0) end
if ddown==true then
MoveClone(-1e4,0,0)
end
if spacedown==true then
reanim.Humanoid.Jump=true end
if wdown ~= true and adown ~= true and sdown ~= true and ddown ~= true then
reanim.Humanoid.WalkToPoint = reanim.HumanoidRootPart.Position end
end))

--reanim.HumanoidRootPart.RootJoint.Part1=nil

workspace.CurrentCamera.CameraSubject = reanim.Humanoid

reset=Instance.new('BindableEvent')
te(ct,reset.Event:Connect(function()
reanim:Destroy()
HumanDied=true
reanimated=false
for i,v in next, char:GetDescendants() do if v:IsA('BasePart') then v.Anchored=true end end
hc=char.Humanoid:Clone()
char.Humanoid:Destroy()
hc.Parent=char
game.Players:Chat('-re')
for i,v in pairs(ct) do v:Disconnect() end
game:GetService("StarterGui"):SetCore("ResetButtonCallback", true)
reset:Remove()
end))

game:GetService("StarterGui"):SetCore("ResetButtonCallback", reset)

IT = Instance.new
CF = CFrame.new
VT = Vector3.new
RAD = math.rad
C3 = Color3.new
UD2 = UDim2.new
BRICKC = BrickColor.new
ANGLES = CFrame.Angles
EULER = CFrame.fromEulerAnglesXYZ
COS = math.cos
ACOS = math.acos
SIN = math.sin
ASIN = math.asin
ABS = math.abs
MRANDOM = math.random
FLOOR = math.floor

speed = 1
sine = 1
srv = game:GetService('RunService')

function hatset(yes,part,c1,c0,nm)
reanim[yes].Handle.AccessoryWeld.Part1=reanim[part]
reanim[yes].Handle.AccessoryWeld.C1=c1 or CFrame.new()
reanim[yes].Handle.AccessoryWeld.C0=c0 or CFrame.new()--3bbb322dad5929d0d4f25adcebf30aa5
if nm==true then
for i,v in next, workspace[game.Players.LocalPlayer.Name][yes].Handle:GetDescendants() do
if v:IsA('Mesh') or v:IsA('SpecialMesh') then
v:Remove()
end
end
end
end

function setuptrail(parent,Pos1,Pos2,Color,LT,LE,Texture)
IT = Instance.new
local Part1 = parent
local A1 = IT("Attachment",Part1)
A1.Position = Pos1
A1.Name = "ATH10"
local B1 = IT("Attachment",Part1)
B1.Position = Pos2
B1.Name = "ATH11"
local Trail1 = IT("Trail",Part1)
Trail1.Name = "Nexo Trail"
Trail1.Color = Color
Trail1.Attachment0 = B1
Trail1.Attachment1 = A1
Trail1.Lifetime = LT
Trail1.LightEmission = LE
Trail1.Transparency = NumberSequence.new({NumberSequenceKeypoint.new(0, 0),NumberSequenceKeypoint.new(1, 1)})
Trail1.Texture = Texture
Trail1.Enabled = true
end

--                          |
--put the setup trail below v

--put the hat script converted below

reanim = game.Players.LocalPlayer.Character.CWExtra.NexoPD
RJ = reanim.HumanoidRootPart.RootJoint
RS = reanim.Torso['Right Shoulder']
LS = reanim.Torso['Left Shoulder']
RH = reanim.Torso['Right Hip']
LH = reanim.Torso['Left Hip']
Root = reanim.HumanoidRootPart
NECK = reanim.Torso.Neck
NECK.C0 = CF(0,1,0)*ANGLES(RAD(0),RAD(0),RAD(0))
NECK.C1 = CF(0,-0.5,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RJ.C1 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RJ.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RS.C1 = CF(-0.5,0.5,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LS.C1 = CF(0.5,0.5,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RH.C1 = CF(0,1,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LH.C1 = CF(0,1,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RH.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LH.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
RS.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))
LS.C0 = CF(0,0,0)*ANGLES(RAD(0),RAD(0),RAD(0))

coroutine.wrap(function()
while true do -- anim changer
if HumanDied then break end
sine = sine + speed
if Root.Velocity.y > 1 then -- jump
--jump clerp here
elseif Root.Velocity.y < -1 then -- fall
--fall clerp here
elseif Root.Velocity.Magnitude < 2 and not dancing and mode == 0 then -- idle
NECK.C0 = NECK.C0:Lerp(CF(1.8+0*math.cos(sine/13),1.4+0.1*math.sin(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(-4+0*math.sin(sine/13)),RAD(-13+0*math.cos(sine/13)),RAD(-2+0*math.sin(sine/13))),.1)
RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),0+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.sin(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13))),.1)
RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.1*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(88+0*math.sin(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(25+0*math.sin(sine/13))),.1)
LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+0.1*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-31+0*math.sin(sine/13)),RAD(3+0*math.cos(sine/13)),RAD(39+0*math.sin(sine/13))),.1)
RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0*math.cos(sine/13),-0.4+0*math.cos(sine/13))*ANGLES(RAD(-2+0*math.sin(sine/13)),RAD(-19+0*math.cos(sine/13)),RAD(-2+0*math.sin(sine/13))),.1)
LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0*math.cos(sine/13),-0.4+0*math.cos(sine/13))*ANGLES(RAD(3+0*math.sin(sine/13)),RAD(18+0*math.cos(sine/13)),RAD(-8+0*math.sin(sine/13))),.1)

elseif Root.Velocity.Magnitude < 20 and not dancing and mode == 0 then -- walk
NECK.C0 = NECK.C0:Lerp(CF(1.8+0*math.cos(sine/13),1.4+0.1*math.sin(sine/13),-0.7+0*math.cos(sine/13))*ANGLES(RAD(-4+0*math.sin(sine/13)),RAD(-13+0*math.cos(sine/13)),RAD(-2+0*math.sin(sine/13))),.1)
RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/13),0+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.sin(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13))),.1)
RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0.1*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(88+0*math.sin(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(25+0*math.sin(sine/13))),.1)
LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+0.1*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-31+0*math.sin(sine/13)),RAD(3+0*math.cos(sine/13)),RAD(39+0*math.sin(sine/13))),.1)
RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0*math.cos(sine/13),-0.4+0*math.cos(sine/13))*ANGLES(RAD(-6+39*math.sin(sine/13)),RAD(-13+0*math.cos(sine/13)),RAD(3+0*math.sin(sine/13))),.1)
LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0*math.cos(sine/13),-0.4+0*math.cos(sine/13))*ANGLES(RAD(-6+-30*math.sin(sine/13)),RAD(18+0*math.cos(sine/13)),RAD(-4+0*math.sin(sine/13))),.1)


elseif Root.Velocity.Magnitude < 2 and dancing then -- idle
NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.sin(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13))),.1)
RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/-36),-1.+0*math.cos(sine/46),0+0*math.cos(sine/-55))*ANGLES(RAD(180+0*math.sin(sine/50)),RAD(-336+290*math.cos(sine/-38)),RAD(0+0*math.sin(sine/68))),.1)
RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(179+0*math.sin(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13))),.1)
LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(183+0*math.sin(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13))),.1)
RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.sin(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(16+0*math.sin(sine/13))),.1)
LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-6+0*math.sin(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(-11+0*math.sin(sine/13))),.1)

elseif Root.Velocity.Magnitude < 20 and dancing then -- walk
NECK.C0 = NECK.C0:Lerp(CF(0+0*math.cos(sine/13),1+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.sin(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13))),.1)
RJ.C0 = RJ.C0:Lerp(CF(0+0*math.cos(sine/-36),-1.+0*math.cos(sine/46),0+0*math.cos(sine/-55))*ANGLES(RAD(180+0*math.sin(sine/50)),RAD(-336+290*math.cos(sine/-38)),RAD(0+0*math.sin(sine/68))),.1)
RS.C0 = RS.C0:Lerp(CF(1+0*math.cos(sine/13),0.5+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(179+0*math.sin(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13))),.1)
LS.C0 = LS.C0:Lerp(CF(-1+0*math.cos(sine/13),0.5+0*math.sin(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(183+0*math.sin(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(0+0*math.sin(sine/13))),.1)
RH.C0 = RH.C0:Lerp(CF(0.5+0*math.cos(sine/13),-1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(0+0*math.sin(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(16+0*math.sin(sine/13))),.1)
LH.C0 = LH.C0:Lerp(CF(-0.5+0*math.cos(sine/13),-1+0*math.cos(sine/13),0+0*math.cos(sine/13))*ANGLES(RAD(-6+0*math.sin(sine/13)),RAD(0+0*math.cos(sine/13)),RAD(-11+0*math.sin(sine/13))),.1)

elseif Root.Velocity.Magnitude > 20 then -- run
--run clerp here
end
srv.RenderStepped:Wait()
end
end)()

m.KeyDown:Connect(function(k)
if k == "t" then
    reanim.Humanoid.WalkSpeed = 16
   dancing = true
end

if k == "r" then
   dancing = false 
end 

if k == "1" then
    reanim.Humanoid.WalkSpeed = 16
   mode = 0 
end 

end)
--Created using Nexo Animator
