---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 2228eb7562ed7a0ffa1c0098086c085985e45fee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259736"
---
# <span data-ttu-id="ac030-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ac030-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="ac030-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac030-102">SYNOPSIS</span></span>
<span data-ttu-id="ac030-103">Skapar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="ac030-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="ac030-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac030-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac030-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac030-105">DESCRIPTION</span></span>
<span data-ttu-id="ac030-106">Cmdleten **New-AzWebAppSlot** skapar en Azure Web App-plats i en given resurs grupp som använder den angivna App Service-abonnemanget och data centret.</span><span class="sxs-lookup"><span data-stu-id="ac030-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="ac030-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac030-107">EXAMPLES</span></span>

### <span data-ttu-id="ac030-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ac030-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="ac030-109">Det här kommandot skapar en kort plats med namnet Slot001 under ett befintligt webbprogram-namn ContosoSite i den befintliga resurs gruppen med namnet default-Web-West i Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="ac030-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="ac030-110">Kommandot använder en befintlig App Service-plan med namnet ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="ac030-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="ac030-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac030-111">PARAMETERS</span></span>

### <span data-ttu-id="ac030-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ac030-112">-AppServicePlan</span></span>
<span data-ttu-id="ac030-113">App Service-planens namn eller ID för App Service-abonnemanget. Om plats-och App Service-abonnemanget finns i olika resurs grupper kan du använda ID istället för namnet.</span><span class="sxs-lookup"><span data-stu-id="ac030-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="ac030-114">App Service-planens ID kan hämtas med: $asp = Get-AzAppServicePlan-ResourceGroup myRGin $asp. ID returnerar App Service plan-ID.</span><span class="sxs-lookup"><span data-stu-id="ac030-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

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

### <span data-ttu-id="ac030-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="ac030-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="ac030-116">Program inställningar åsidosätter hash</span><span class="sxs-lookup"><span data-stu-id="ac030-116">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac030-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="ac030-117">-AseName</span></span>
<span data-ttu-id="ac030-118">App Service Environment</span><span class="sxs-lookup"><span data-stu-id="ac030-118">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac030-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac030-119">-AseResourceGroupName</span></span>
<span data-ttu-id="ac030-120">App Service Environment resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="ac030-120">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac030-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac030-121">-AsJob</span></span>
<span data-ttu-id="ac030-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ac030-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac030-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="ac030-123">-ContainerImageName</span></span>
<span data-ttu-id="ac030-124">Namn på behållare och valfri tagg, till exempel (bild: tagg)</span><span class="sxs-lookup"><span data-stu-id="ac030-124">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac030-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="ac030-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="ac030-126">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="ac030-126">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac030-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="ac030-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="ac030-128">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="ac030-128">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac030-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="ac030-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="ac030-130">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="ac030-130">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac030-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac030-131">-DefaultProfile</span></span>
<span data-ttu-id="ac030-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac030-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac030-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="ac030-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="ac030-134">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="ac030-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="ac030-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="ac030-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="ac030-136">Alternativet Ignorera anpassade värd namn</span><span class="sxs-lookup"><span data-stu-id="ac030-136">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac030-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="ac030-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="ac030-138">Alternativet Ignorera käll kontroll</span><span class="sxs-lookup"><span data-stu-id="ac030-138">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac030-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="ac030-139">-Name</span></span>
<span data-ttu-id="ac030-140">Webapp-namn</span><span class="sxs-lookup"><span data-stu-id="ac030-140">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac030-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac030-141">-ResourceGroupName</span></span>
<span data-ttu-id="ac030-142">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ac030-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac030-143">-Plats</span><span class="sxs-lookup"><span data-stu-id="ac030-143">-Slot</span></span>
<span data-ttu-id="ac030-144">Webapp-slot</span><span class="sxs-lookup"><span data-stu-id="ac030-144">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac030-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="ac030-145">-SourceWebApp</span></span>
<span data-ttu-id="ac030-146">Source WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="ac030-146">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac030-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac030-147">CommonParameters</span></span>
<span data-ttu-id="ac030-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac030-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac030-149">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac030-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac030-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac030-150">INPUTS</span></span>

### <span data-ttu-id="ac030-151">System. String</span><span class="sxs-lookup"><span data-stu-id="ac030-151">System.String</span></span>

### <span data-ttu-id="ac030-152">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ac030-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ac030-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac030-153">OUTPUTS</span></span>

### <span data-ttu-id="ac030-154">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="ac030-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ac030-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac030-155">NOTES</span></span>

## <span data-ttu-id="ac030-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac030-156">RELATED LINKS</span></span>

[<span data-ttu-id="ac030-157">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ac030-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="ac030-158">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ac030-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="ac030-159">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ac030-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="ac030-160">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ac030-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="ac030-161">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ac030-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="ac030-162">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ac030-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="ac030-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ac030-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="ac030-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ac030-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
