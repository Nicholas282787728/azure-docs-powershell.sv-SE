---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 6c7fbd4512bfac7a369f21f85803653c6f7c9628
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583372"
---
# <span data-ttu-id="b0500-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0500-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="b0500-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0500-102">SYNOPSIS</span></span>
<span data-ttu-id="b0500-103">Skapar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="b0500-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0500-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0500-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0500-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0500-105">DESCRIPTION</span></span>
<span data-ttu-id="b0500-106">Cmdleten **New-AzureRmWebAppSlot** skapar en Azure Web App-plats i en given resurs grupp som använder den angivna App Service-abonnemanget och data centret.</span><span class="sxs-lookup"><span data-stu-id="b0500-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="b0500-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0500-107">EXAMPLES</span></span>

### <span data-ttu-id="b0500-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b0500-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="b0500-109">Det här kommandot skapar en kort plats med namnet Slot001 under ett befintligt webbprogram-namn ContosoSite i den befintliga resurs gruppen med namnet default-Web-West i Data Center West US.</span><span class="sxs-lookup"><span data-stu-id="b0500-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="b0500-110">Kommandot använder en befintlig App Service-plan med namnet ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="b0500-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="b0500-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0500-111">PARAMETERS</span></span>

### <span data-ttu-id="b0500-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b0500-112">-AppServicePlan</span></span>
<span data-ttu-id="b0500-113">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="b0500-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="b0500-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="b0500-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="b0500-115">Program inställningar åsidosätter hash</span><span class="sxs-lookup"><span data-stu-id="b0500-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="b0500-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="b0500-116">-AseName</span></span>
<span data-ttu-id="b0500-117">App Service Environment</span><span class="sxs-lookup"><span data-stu-id="b0500-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="b0500-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0500-118">-AseResourceGroupName</span></span>
<span data-ttu-id="b0500-119">App Service Environment resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="b0500-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="b0500-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0500-120">-AsJob</span></span>
<span data-ttu-id="b0500-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b0500-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0500-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="b0500-122">-ContainerImageName</span></span>
<span data-ttu-id="b0500-123">Namn på behållare och valfri tagg, till exempel (bild: tagg)</span><span class="sxs-lookup"><span data-stu-id="b0500-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="b0500-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="b0500-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="b0500-125">Lösen ord för privat behållare</span><span class="sxs-lookup"><span data-stu-id="b0500-125">Private Container Registry Password</span></span>

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

### <span data-ttu-id="b0500-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="b0500-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="b0500-127">Webb adress för privat behållarens register Server</span><span class="sxs-lookup"><span data-stu-id="b0500-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="b0500-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="b0500-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="b0500-129">Användar namn för privat behållare</span><span class="sxs-lookup"><span data-stu-id="b0500-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="b0500-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0500-130">-DefaultProfile</span></span>
<span data-ttu-id="b0500-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0500-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0500-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="b0500-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="b0500-133">Aktiverar/inaktiverar kontinuerlig distribution av behållare webhook</span><span class="sxs-lookup"><span data-stu-id="b0500-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="b0500-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="b0500-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="b0500-135">Alternativet Ignorera anpassade värd namn</span><span class="sxs-lookup"><span data-stu-id="b0500-135">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="b0500-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="b0500-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="b0500-137">Alternativet Ignorera käll kontroll</span><span class="sxs-lookup"><span data-stu-id="b0500-137">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="b0500-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0500-138">-Name</span></span>
<span data-ttu-id="b0500-139">Webapp-namn</span><span class="sxs-lookup"><span data-stu-id="b0500-139">Webapp Name</span></span>

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

### <span data-ttu-id="b0500-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0500-140">-ResourceGroupName</span></span>
<span data-ttu-id="b0500-141">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b0500-141">Resource Group Name</span></span>

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

### <span data-ttu-id="b0500-142">-Plats</span><span class="sxs-lookup"><span data-stu-id="b0500-142">-Slot</span></span>
<span data-ttu-id="b0500-143">Webapp-slot</span><span class="sxs-lookup"><span data-stu-id="b0500-143">Webapp Slot Name</span></span>

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

### <span data-ttu-id="b0500-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="b0500-144">-SourceWebApp</span></span>
<span data-ttu-id="b0500-145">Source WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="b0500-145">Source WebApp Object</span></span>

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

### <span data-ttu-id="b0500-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0500-146">CommonParameters</span></span>
<span data-ttu-id="b0500-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0500-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0500-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0500-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0500-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0500-149">INPUTS</span></span>

### <span data-ttu-id="b0500-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b0500-150">System.String</span></span>

### <span data-ttu-id="b0500-151">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="b0500-151">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="b0500-152">Parametrar: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b0500-152">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="b0500-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0500-153">OUTPUTS</span></span>

### <span data-ttu-id="b0500-154">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="b0500-154">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="b0500-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0500-155">NOTES</span></span>

## <span data-ttu-id="b0500-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0500-156">RELATED LINKS</span></span>

[<span data-ttu-id="b0500-157">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0500-157">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="b0500-158">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0500-158">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="b0500-159">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0500-159">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="b0500-160">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0500-160">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="b0500-161">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0500-161">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="b0500-162">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0500-162">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="b0500-163">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b0500-163">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="b0500-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b0500-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
