---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 8120b22f02d137ff261b1b4e345b917d6ae82a5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746068"
---
# <span data-ttu-id="0e9f5-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0e9f5-101">New-AzWebApp</span></span>

## <span data-ttu-id="0e9f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e9f5-102">SYNOPSIS</span></span>
<span data-ttu-id="0e9f5-103">Skapar ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0e9f5-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="0e9f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e9f5-104">SYNTAX</span></span>

### <span data-ttu-id="0e9f5-105">SimpleParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0e9f5-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e9f5-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="0e9f5-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e9f5-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e9f5-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e9f5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e9f5-108">DESCRIPTION</span></span>
<span data-ttu-id="0e9f5-109">Cmdleten **New-AzWebApp** skapar ett Azure Web App i en given resurs grupp som använder den angivna App Service-abonnemanget och data centret.</span><span class="sxs-lookup"><span data-stu-id="0e9f5-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="0e9f5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e9f5-110">EXAMPLES</span></span>

### <span data-ttu-id="0e9f5-111">Exempel 1: skapa ett webb program</span><span class="sxs-lookup"><span data-stu-id="0e9f5-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="0e9f5-112">Det här kommandot skapar ett Azure Web App-objekt med namnet ContosoSite i den befintliga resurs gruppen som heter default-West-väster in data Center.</span><span class="sxs-lookup"><span data-stu-id="0e9f5-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="0e9f5-113">Kommandot använder en befintlig App Service-plan med namnet ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="0e9f5-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="0e9f5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e9f5-114">PARAMETERS</span></span>

### <span data-ttu-id="0e9f5-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0e9f5-115">-AppServicePlan</span></span>
<span data-ttu-id="0e9f5-116">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="0e9f5-116">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-117">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="0e9f5-117">-AppSettingsOverrides</span></span>
<span data-ttu-id="0e9f5-118">Program inställningar åsidosätter hash</span><span class="sxs-lookup"><span data-stu-id="0e9f5-118">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-119">-AseName</span><span class="sxs-lookup"><span data-stu-id="0e9f5-119">-AseName</span></span>
<span data-ttu-id="0e9f5-120">App Service Environment</span><span class="sxs-lookup"><span data-stu-id="0e9f5-120">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-121">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e9f5-121">-AseResourceGroupName</span></span>
<span data-ttu-id="0e9f5-122">App Service Environment resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="0e9f5-122">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e9f5-123">-AsJob</span></span>
<span data-ttu-id="0e9f5-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0e9f5-124">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="0e9f5-125">-ContainerImageName</span></span>
<span data-ttu-id="0e9f5-126">Namn på behållare och valfri tagg, till exempel (bild: tagg)</span><span class="sxs-lookup"><span data-stu-id="0e9f5-126">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="0e9f5-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="0e9f5-128">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="0e9f5-128">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="0e9f5-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="0e9f5-130">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="0e9f5-130">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="0e9f5-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="0e9f5-132">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="0e9f5-132">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e9f5-133">-DefaultProfile</span></span>
<span data-ttu-id="0e9f5-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e9f5-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-135">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="0e9f5-135">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="0e9f5-136">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="0e9f5-136">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-137">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="0e9f5-137">-GitRepositoryPath</span></span>
<span data-ttu-id="0e9f5-138">Sökvägen till GitHub-databasen som innehåller webb programmet som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="0e9f5-138">Path to the GitHub repository containing the web application to deploy.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-139">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="0e9f5-139">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="0e9f5-140">Ignorera anpassade värd namns alternativ</span><span class="sxs-lookup"><span data-stu-id="0e9f5-140">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-141">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="0e9f5-141">-IgnoreSourceControl</span></span>
<span data-ttu-id="0e9f5-142">Alternativet Ignorera käll kontroll</span><span class="sxs-lookup"><span data-stu-id="0e9f5-142">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-143">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="0e9f5-143">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="0e9f5-144">Inkludera alternativet Source WebApp-fack</span><span class="sxs-lookup"><span data-stu-id="0e9f5-144">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-145">-Plats</span><span class="sxs-lookup"><span data-stu-id="0e9f5-145">-Location</span></span>
<span data-ttu-id="0e9f5-146">Plats</span><span class="sxs-lookup"><span data-stu-id="0e9f5-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e9f5-147">-Name</span></span>
<span data-ttu-id="0e9f5-148">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="0e9f5-148">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e9f5-149">-ResourceGroupName</span></span>
<span data-ttu-id="0e9f5-150">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="0e9f5-150">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry, WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-151">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="0e9f5-151">-SourceWebApp</span></span>
<span data-ttu-id="0e9f5-152">Source WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="0e9f5-152">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-153">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0e9f5-153">-TrafficManagerProfile</span></span>
<span data-ttu-id="0e9f5-154">Resurs-ID för befintlig Traffic Manager-profil</span><span class="sxs-lookup"><span data-stu-id="0e9f5-154">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0e9f5-155">-Confirm</span></span>
<span data-ttu-id="0e9f5-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0e9f5-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e9f5-157">-WhatIf</span></span>
<span data-ttu-id="0e9f5-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0e9f5-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e9f5-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0e9f5-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9f5-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e9f5-160">CommonParameters</span></span>
<span data-ttu-id="0e9f5-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e9f5-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e9f5-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e9f5-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e9f5-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e9f5-163">INPUTS</span></span>

### <span data-ttu-id="0e9f5-164">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0e9f5-164">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0e9f5-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e9f5-165">OUTPUTS</span></span>

### <span data-ttu-id="0e9f5-166">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0e9f5-166">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0e9f5-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e9f5-167">NOTES</span></span>

## <span data-ttu-id="0e9f5-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e9f5-168">RELATED LINKS</span></span>

[<span data-ttu-id="0e9f5-169">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0e9f5-169">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="0e9f5-170">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0e9f5-170">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="0e9f5-171">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0e9f5-171">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="0e9f5-172">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0e9f5-172">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="0e9f5-173">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0e9f5-173">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


