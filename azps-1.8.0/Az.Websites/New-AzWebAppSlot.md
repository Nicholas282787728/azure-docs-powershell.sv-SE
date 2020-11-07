---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 941de31e1733bd591507176216e30f9e1510f706
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746051"
---
# <span data-ttu-id="554c5-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="554c5-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="554c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="554c5-102">SYNOPSIS</span></span>
<span data-ttu-id="554c5-103">Skapar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="554c5-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="554c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="554c5-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="554c5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="554c5-105">DESCRIPTION</span></span>
<span data-ttu-id="554c5-106">Cmdleten **New-AzWebAppSlot** skapar en Azure Web App-plats i en given resurs grupp som använder den angivna App Service-abonnemanget och data centret.</span><span class="sxs-lookup"><span data-stu-id="554c5-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="554c5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="554c5-107">EXAMPLES</span></span>

### <span data-ttu-id="554c5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="554c5-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="554c5-109">Det här kommandot skapar en kort plats med namnet Slot001 under ett befintligt webbprogram-namn ContosoSite i den befintliga resurs gruppen med namnet default-Web-West i Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="554c5-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="554c5-110">Kommandot använder en befintlig App Service-plan med namnet ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="554c5-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="554c5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="554c5-111">PARAMETERS</span></span>

### <span data-ttu-id="554c5-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="554c5-112">-AppServicePlan</span></span>
<span data-ttu-id="554c5-113">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="554c5-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="554c5-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="554c5-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="554c5-115">Program inställningar åsidosätter hash</span><span class="sxs-lookup"><span data-stu-id="554c5-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="554c5-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="554c5-116">-AseName</span></span>
<span data-ttu-id="554c5-117">App Service Environment</span><span class="sxs-lookup"><span data-stu-id="554c5-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="554c5-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="554c5-118">-AseResourceGroupName</span></span>
<span data-ttu-id="554c5-119">App Service Environment resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="554c5-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="554c5-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="554c5-120">-AsJob</span></span>
<span data-ttu-id="554c5-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="554c5-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="554c5-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="554c5-122">-ContainerImageName</span></span>
<span data-ttu-id="554c5-123">Namn på behållare och valfri tagg, till exempel (bild: tagg)</span><span class="sxs-lookup"><span data-stu-id="554c5-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="554c5-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="554c5-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="554c5-125">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="554c5-125">Private Container Registry Password</span></span>

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

### <span data-ttu-id="554c5-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="554c5-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="554c5-127">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="554c5-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="554c5-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="554c5-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="554c5-129">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="554c5-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="554c5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="554c5-130">-DefaultProfile</span></span>
<span data-ttu-id="554c5-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="554c5-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="554c5-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="554c5-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="554c5-133">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="554c5-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="554c5-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="554c5-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="554c5-135">Alternativet Ignorera anpassade värd namn</span><span class="sxs-lookup"><span data-stu-id="554c5-135">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="554c5-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="554c5-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="554c5-137">Alternativet Ignorera käll kontroll</span><span class="sxs-lookup"><span data-stu-id="554c5-137">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="554c5-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="554c5-138">-Name</span></span>
<span data-ttu-id="554c5-139">Webapp-namn</span><span class="sxs-lookup"><span data-stu-id="554c5-139">Webapp Name</span></span>

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

### <span data-ttu-id="554c5-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="554c5-140">-ResourceGroupName</span></span>
<span data-ttu-id="554c5-141">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="554c5-141">Resource Group Name</span></span>

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

### <span data-ttu-id="554c5-142">-Plats</span><span class="sxs-lookup"><span data-stu-id="554c5-142">-Slot</span></span>
<span data-ttu-id="554c5-143">Webapp-slot</span><span class="sxs-lookup"><span data-stu-id="554c5-143">Webapp Slot Name</span></span>

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

### <span data-ttu-id="554c5-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="554c5-144">-SourceWebApp</span></span>
<span data-ttu-id="554c5-145">Source WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="554c5-145">Source WebApp Object</span></span>

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

### <span data-ttu-id="554c5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="554c5-146">CommonParameters</span></span>
<span data-ttu-id="554c5-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="554c5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="554c5-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="554c5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="554c5-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="554c5-149">INPUTS</span></span>

### <span data-ttu-id="554c5-150">System. String</span><span class="sxs-lookup"><span data-stu-id="554c5-150">System.String</span></span>

### <span data-ttu-id="554c5-151">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="554c5-151">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="554c5-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="554c5-152">OUTPUTS</span></span>

### <span data-ttu-id="554c5-153">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="554c5-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="554c5-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="554c5-154">NOTES</span></span>

## <span data-ttu-id="554c5-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="554c5-155">RELATED LINKS</span></span>

[<span data-ttu-id="554c5-156">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="554c5-156">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="554c5-157">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="554c5-157">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="554c5-158">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="554c5-158">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="554c5-159">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="554c5-159">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="554c5-160">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="554c5-160">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="554c5-161">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="554c5-161">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="554c5-162">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="554c5-162">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="554c5-163">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="554c5-163">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
