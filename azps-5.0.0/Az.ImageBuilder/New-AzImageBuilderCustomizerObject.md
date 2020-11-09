---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319519"
---
# <span data-ttu-id="6b717-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="6b717-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="6b717-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b717-102">SYNOPSIS</span></span>
<span data-ttu-id="6b717-103">Beskriver en enhet med bild anpassning</span><span class="sxs-lookup"><span data-stu-id="6b717-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="6b717-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b717-104">SYNTAX</span></span>

### <span data-ttu-id="6b717-105">ShellCustomizer (standard)</span><span class="sxs-lookup"><span data-stu-id="6b717-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="6b717-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="6b717-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="6b717-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="6b717-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b717-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="6b717-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="6b717-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="6b717-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6b717-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b717-110">DESCRIPTION</span></span>
<span data-ttu-id="6b717-111">Beskriver en enhet med bild anpassning</span><span class="sxs-lookup"><span data-stu-id="6b717-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="6b717-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b717-112">EXAMPLES</span></span>

### <span data-ttu-id="6b717-113">Exempel 1: skapa en Windows Update-anpassare</span><span class="sxs-lookup"><span data-stu-id="6b717-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="6b717-114">Det här kommandot skapar en Windows Update-anpassning.</span><span class="sxs-lookup"><span data-stu-id="6b717-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="6b717-115">Exempel 2: skapa en fil anpassning</span><span class="sxs-lookup"><span data-stu-id="6b717-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="6b717-116">Det här kommandot skapar en fil anpassning.</span><span class="sxs-lookup"><span data-stu-id="6b717-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="6b717-117">Exempel 3: skapa en PowerShell-anpassare</span><span class="sxs-lookup"><span data-stu-id="6b717-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="6b717-118">Det här kommandot skapar en PowerShell-anpassare.</span><span class="sxs-lookup"><span data-stu-id="6b717-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="6b717-119">Exempel 4: skapa en omstarts anpassare</span><span class="sxs-lookup"><span data-stu-id="6b717-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="6b717-120">Det här kommandot skapar en starta om-anpassning.</span><span class="sxs-lookup"><span data-stu-id="6b717-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="6b717-121">Exempel 5: skapa en Shell-anpassning</span><span class="sxs-lookup"><span data-stu-id="6b717-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="6b717-122">Det här kommandot skapar en Shell-anpassning.</span><span class="sxs-lookup"><span data-stu-id="6b717-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="6b717-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b717-123">PARAMETERS</span></span>

### <span data-ttu-id="6b717-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="6b717-124">-CustomizerName</span></span>
<span data-ttu-id="6b717-125">Eget namn för att ange sammanhang för det här anpassade steget.</span><span class="sxs-lookup"><span data-stu-id="6b717-125">Friendly Name to provide context on what this customization step does.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-126">-Mål</span><span class="sxs-lookup"><span data-stu-id="6b717-126">-Destination</span></span>
<span data-ttu-id="6b717-127">Den absoluta sökvägen till en fil (med kapslade katalog strukturer som redan har skapats) där filen (från sourceUri) ska laddas upp till i den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6b717-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="6b717-128">-FileCustomizer</span></span>
<span data-ttu-id="6b717-129">Uppladdar filer till virtuella datorer (Linux, Windows).</span><span class="sxs-lookup"><span data-stu-id="6b717-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="6b717-130">Motsvarar programetableringen för programvaran.</span><span class="sxs-lookup"><span data-stu-id="6b717-130">Corresponds to Packer file provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="6b717-131">-Filter</span></span>
<span data-ttu-id="6b717-132">Matris med filter för att välja vilka uppdateringar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6b717-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="6b717-133">Utelämna eller ange en tom matris för att använda standardvärdet (Nej).</span><span class="sxs-lookup"><span data-stu-id="6b717-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="6b717-134">Se ovan-länken för exempel och detaljerad beskrivning av det här fältet.</span><span class="sxs-lookup"><span data-stu-id="6b717-134">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-135">Infogad</span><span class="sxs-lookup"><span data-stu-id="6b717-135">-Inline</span></span>
<span data-ttu-id="6b717-136">Matris med skal kommandon att köra.</span><span class="sxs-lookup"><span data-stu-id="6b717-136">Array of shell commands to execute.</span></span>

```yaml
Type: System.String[]
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="6b717-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="6b717-138">Kör den angivna PowerShell-tjänsten på den virtuella datorn (Windows).</span><span class="sxs-lookup"><span data-stu-id="6b717-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="6b717-139">Korresponderar med PowerShell-etableringen för paket.</span><span class="sxs-lookup"><span data-stu-id="6b717-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="6b717-140">Exakt en av "scriptUri" eller "infogad" kan anges.</span><span class="sxs-lookup"><span data-stu-id="6b717-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PowerShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="6b717-141">-RestartCheckCommand</span></span>
<span data-ttu-id="6b717-142">Om du vill kontrol lera om restart lyckades [standard: "'].</span><span class="sxs-lookup"><span data-stu-id="6b717-142">Command to check if restart succeeded [Default: ''].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="6b717-143">-RestartCommand</span></span>
<span data-ttu-id="6b717-144">Kommando för att köra starta om [standard: "shutdown/r/f/t 0/c-Paketeraren restart"]</span><span class="sxs-lookup"><span data-stu-id="6b717-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="6b717-145">-RestartCustomizer</span></span>
<span data-ttu-id="6b717-146">Startar om en virtuell dator och väntar på att den ska vara online (Windows) igen.</span><span class="sxs-lookup"><span data-stu-id="6b717-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="6b717-147">Motsvarar programpackaren Windows-restart-etableringen.</span><span class="sxs-lookup"><span data-stu-id="6b717-147">Corresponds to Packer windows-restart provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestartCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="6b717-148">-RestartTimeout</span></span>
<span data-ttu-id="6b717-149">Timeout för omstart angiven som en text sträng, till exempel "5 milj" (5 minuter) eller "2H" (2 timmar) [standard: "5 milj"].</span><span class="sxs-lookup"><span data-stu-id="6b717-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="6b717-150">-RunElevated</span></span>
<span data-ttu-id="6b717-151">Om det anges körs PowerShell-skriptet med förhöjda behörigheter.</span><span class="sxs-lookup"><span data-stu-id="6b717-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="6b717-152">-ScriptUri</span></span>
<span data-ttu-id="6b717-153">URI för Shell-skript som ska köras för anpassning.</span><span class="sxs-lookup"><span data-stu-id="6b717-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="6b717-154">Det kan vara en GitHub-länk, SAS URI för Azure Storage etc.</span><span class="sxs-lookup"><span data-stu-id="6b717-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="6b717-155">-SearchCriterion</span></span>
<span data-ttu-id="6b717-156">Villkor för Sök uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="6b717-156">Criteria to search updates.</span></span>
<span data-ttu-id="6b717-157">Utelämna eller ange en tom sträng om du vill använda standardvärdet (Sök alla).</span><span class="sxs-lookup"><span data-stu-id="6b717-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="6b717-158">Se ovan-länken för exempel och detaljerad beskrivning av det här fältet.</span><span class="sxs-lookup"><span data-stu-id="6b717-158">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="6b717-159">-Sha256Checksum</span></span>
<span data-ttu-id="6b717-160">SHA256 kontroll summa för Shell-skriptet i fältet scriptUri.</span><span class="sxs-lookup"><span data-stu-id="6b717-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer, PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="6b717-161">-ShellCustomizer</span></span>
<span data-ttu-id="6b717-162">Kör ett skal skript under anpassnings fasen (Linux).</span><span class="sxs-lookup"><span data-stu-id="6b717-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="6b717-163">Motsvarar programetableringen för programpaketet.</span><span class="sxs-lookup"><span data-stu-id="6b717-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="6b717-164">Exakt en av "scriptUri" eller "infogad" kan anges.</span><span class="sxs-lookup"><span data-stu-id="6b717-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="6b717-165">-SourceUri</span></span>
<span data-ttu-id="6b717-166">URI för filen som ska laddas upp för anpassning av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6b717-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="6b717-167">Det kan vara en GitHub-länk, SAS URI för Azure Storage etc.</span><span class="sxs-lookup"><span data-stu-id="6b717-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="6b717-168">-UpdateLimit</span></span>
<span data-ttu-id="6b717-169">Maximalt antal uppdateringar att lägga till åt gången.</span><span class="sxs-lookup"><span data-stu-id="6b717-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="6b717-170">Utelämna eller ange 0 för att använda standardvärdet (1000).</span><span class="sxs-lookup"><span data-stu-id="6b717-170">Omit or specify 0 to use the default (1000).</span></span>

```yaml
Type: System.Int32
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="6b717-171">-ValidExitCode</span></span>
<span data-ttu-id="6b717-172">Giltiga slutkod för PowerShell-skriptet.</span><span class="sxs-lookup"><span data-stu-id="6b717-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="6b717-173">[Standard: 0].</span><span class="sxs-lookup"><span data-stu-id="6b717-173">[Default: 0].</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="6b717-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="6b717-175">Installerar Windows-uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="6b717-175">Installs Windows Updates.</span></span>
<span data-ttu-id="6b717-176">Motsvarar programetableringen för packaren ( https://github.com/rgl/packer-provisioner-windows-update) .</span><span class="sxs-lookup"><span data-stu-id="6b717-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b717-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b717-177">CommonParameters</span></span>
<span data-ttu-id="6b717-178">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b717-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b717-179">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b717-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b717-180">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b717-180">INPUTS</span></span>

## <span data-ttu-id="6b717-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b717-181">OUTPUTS</span></span>

### <span data-ttu-id="6b717-182">Microsoft. Azure. PowerShell. cmdletar. ImageBuilder. Models. Api20200214. IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="6b717-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="6b717-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b717-183">NOTES</span></span>

<span data-ttu-id="6b717-184">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6b717-184">ALIASES</span></span>

## <span data-ttu-id="6b717-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b717-185">RELATED LINKS</span></span>

