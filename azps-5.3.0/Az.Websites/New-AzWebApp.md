---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 760aacba880276059c4a468454cccec29d397183
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522105"
---
# <span data-ttu-id="1b9ec-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1b9ec-101">New-AzWebApp</span></span>

## <span data-ttu-id="1b9ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1b9ec-103">Skapar ett Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="1b9ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b9ec-104">SYNTAX</span></span>

### <span data-ttu-id="1b9ec-105">SimpleParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1b9ec-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b9ec-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="1b9ec-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b9ec-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b9ec-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b9ec-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b9ec-108">DESCRIPTION</span></span>
<span data-ttu-id="1b9ec-109">Cmdleten **New-AzWebApp** skapar ett Azure Web App i en given resurs grupp som använder den angivna App Service-abonnemanget och data centret.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="1b9ec-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b9ec-110">EXAMPLES</span></span>

### <span data-ttu-id="1b9ec-111">Exempel 1: skapa ett webb program</span><span class="sxs-lookup"><span data-stu-id="1b9ec-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="1b9ec-112">Det här kommandot skapar ett Azure Web App-objekt med namnet ContosoSite i den befintliga resurs gruppen som heter default-West-väster in data Center.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="1b9ec-113">Kommandot använder en befintlig App Service-plan med namnet ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="1b9ec-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b9ec-114">PARAMETERS</span></span>

### <span data-ttu-id="1b9ec-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1b9ec-115">-AppServicePlan</span></span>
<span data-ttu-id="1b9ec-116">App Service-planens namn eller ID för App Service-abonnemanget. Om ett WebApp-och App Service-abonnemang finns i olika resurs grupper kan du använda ID istället för namnet.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="1b9ec-117">App Service-planens ID kan hämtas med: $asp = Get-AzAppServicePlan-ResourceGroup myRGin $asp. ID returnerar App Service plan-ID.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


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

### <span data-ttu-id="1b9ec-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="1b9ec-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="1b9ec-119">Program inställningar åsidosätter hash</span><span class="sxs-lookup"><span data-stu-id="1b9ec-119">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="1b9ec-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="1b9ec-120">-AseName</span></span>
<span data-ttu-id="1b9ec-121">App Service Environment</span><span class="sxs-lookup"><span data-stu-id="1b9ec-121">App Service Environment Name</span></span>

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

### <span data-ttu-id="1b9ec-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b9ec-122">-AseResourceGroupName</span></span>
<span data-ttu-id="1b9ec-123">App Service Environment resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="1b9ec-123">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="1b9ec-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b9ec-124">-AsJob</span></span>
<span data-ttu-id="1b9ec-125">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1b9ec-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b9ec-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="1b9ec-126">-ContainerImageName</span></span>
<span data-ttu-id="1b9ec-127">Namn på behållare och valfri tagg, till exempel (bild: tagg)</span><span class="sxs-lookup"><span data-stu-id="1b9ec-127">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="1b9ec-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="1b9ec-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="1b9ec-129">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="1b9ec-129">Private Container Registry Password</span></span>

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

### <span data-ttu-id="1b9ec-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="1b9ec-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="1b9ec-131">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="1b9ec-131">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="1b9ec-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="1b9ec-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="1b9ec-133">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="1b9ec-133">Private Container Registry Username</span></span>

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

### <span data-ttu-id="1b9ec-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b9ec-134">-DefaultProfile</span></span>
<span data-ttu-id="1b9ec-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b9ec-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="1b9ec-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="1b9ec-137">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="1b9ec-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="1b9ec-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="1b9ec-138">-GitRepositoryPath</span></span>
<span data-ttu-id="1b9ec-139">Sökvägen till GitHub-databasen som innehåller webb programmet som ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-139">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="1b9ec-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="1b9ec-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="1b9ec-141">Ignorera anpassade värd namns alternativ</span><span class="sxs-lookup"><span data-stu-id="1b9ec-141">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="1b9ec-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="1b9ec-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="1b9ec-143">Alternativet Ignorera käll kontroll</span><span class="sxs-lookup"><span data-stu-id="1b9ec-143">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="1b9ec-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="1b9ec-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="1b9ec-145">Inkludera alternativet Source WebApp-fack</span><span class="sxs-lookup"><span data-stu-id="1b9ec-145">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="1b9ec-146">-Plats</span><span class="sxs-lookup"><span data-stu-id="1b9ec-146">-Location</span></span>
<span data-ttu-id="1b9ec-147">Plats</span><span class="sxs-lookup"><span data-stu-id="1b9ec-147">Location</span></span>

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

### <span data-ttu-id="1b9ec-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b9ec-148">-Name</span></span>
<span data-ttu-id="1b9ec-149">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="1b9ec-149">WebApp Name</span></span>

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

### <span data-ttu-id="1b9ec-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b9ec-150">-ResourceGroupName</span></span>
<span data-ttu-id="1b9ec-151">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="1b9ec-151">Resource Group Name</span></span>

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

### <span data-ttu-id="1b9ec-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="1b9ec-152">-SourceWebApp</span></span>
<span data-ttu-id="1b9ec-153">Source WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="1b9ec-153">Source WebApp Object</span></span>

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

### <span data-ttu-id="1b9ec-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1b9ec-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="1b9ec-155">Resurs-ID för befintlig Traffic Manager-profil</span><span class="sxs-lookup"><span data-stu-id="1b9ec-155">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="1b9ec-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1b9ec-156">-Confirm</span></span>
<span data-ttu-id="1b9ec-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b9ec-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b9ec-158">-WhatIf</span></span>
<span data-ttu-id="1b9ec-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b9ec-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b9ec-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b9ec-161">CommonParameters</span></span>
<span data-ttu-id="1b9ec-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b9ec-163">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b9ec-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b9ec-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b9ec-164">INPUTS</span></span>

### <span data-ttu-id="1b9ec-165">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1b9ec-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1b9ec-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b9ec-166">OUTPUTS</span></span>

### <span data-ttu-id="1b9ec-167">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1b9ec-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1b9ec-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b9ec-168">NOTES</span></span>

## <span data-ttu-id="1b9ec-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b9ec-169">RELATED LINKS</span></span>

[<span data-ttu-id="1b9ec-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1b9ec-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="1b9ec-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1b9ec-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="1b9ec-172">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1b9ec-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="1b9ec-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1b9ec-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="1b9ec-174">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1b9ec-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


