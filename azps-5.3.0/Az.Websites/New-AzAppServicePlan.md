---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: af94f1bec48bf54284ccf6e0011753a737dac30b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522110"
---
# <span data-ttu-id="206ad-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="206ad-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="206ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="206ad-102">SYNOPSIS</span></span>
<span data-ttu-id="206ad-103">Skapar en Azure App Service-plan på en given Geo-plats.</span><span class="sxs-lookup"><span data-stu-id="206ad-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="206ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="206ad-104">SYNTAX</span></span>

### <span data-ttu-id="206ad-105">S</span><span class="sxs-lookup"><span data-stu-id="206ad-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="206ad-106">S2</span><span class="sxs-lookup"><span data-stu-id="206ad-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="206ad-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="206ad-107">DESCRIPTION</span></span>
<span data-ttu-id="206ad-108">Cmdleten **New-AzAppServicePlan** skapar en Azure App Service-plan på en given Geo-plats med den angivna nivån, arbetarens arbets storlek och antalet arbetare.</span><span class="sxs-lookup"><span data-stu-id="206ad-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="206ad-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="206ad-109">EXAMPLES</span></span>

### <span data-ttu-id="206ad-110">Exempel 1: skapa en app service-plan</span><span class="sxs-lookup"><span data-stu-id="206ad-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="206ad-111">Det här kommandot skapar en app service-plan med namnet ContosoASP i resurs gruppen som heter default-West-väst på Geo-platsen.</span><span class="sxs-lookup"><span data-stu-id="206ad-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="206ad-112">Kommandot anger en enkel nivå och tilldelar två små arbets tagare.</span><span class="sxs-lookup"><span data-stu-id="206ad-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="206ad-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="206ad-113">PARAMETERS</span></span>

### <span data-ttu-id="206ad-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="206ad-114">-AppServicePlan</span></span>
<span data-ttu-id="206ad-115">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="206ad-115">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="206ad-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="206ad-116">-AseName</span></span>
<span data-ttu-id="206ad-117">App Service Environment</span><span class="sxs-lookup"><span data-stu-id="206ad-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206ad-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="206ad-118">-AseResourceGroupName</span></span>
<span data-ttu-id="206ad-119">App Service Environment resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="206ad-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206ad-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="206ad-120">-AsJob</span></span>
<span data-ttu-id="206ad-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="206ad-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="206ad-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="206ad-122">-DefaultProfile</span></span>
<span data-ttu-id="206ad-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="206ad-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="206ad-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="206ad-124">-HyperV</span></span>
<span data-ttu-id="206ad-125">Ange detta program tjänst abonnemang kör Windows-behållare</span><span class="sxs-lookup"><span data-stu-id="206ad-125">Specify this, App Service Plan will run Windows Containers</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206ad-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="206ad-126">-Location</span></span>
<span data-ttu-id="206ad-127">Plats</span><span class="sxs-lookup"><span data-stu-id="206ad-127">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206ad-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="206ad-128">-Name</span></span>
<span data-ttu-id="206ad-129">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="206ad-129">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206ad-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="206ad-130">-NumberofWorkers</span></span>
<span data-ttu-id="206ad-131">Antal arbetare</span><span class="sxs-lookup"><span data-stu-id="206ad-131">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206ad-132">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="206ad-132">-PerSiteScaling</span></span>
<span data-ttu-id="206ad-133">Om du vill aktivera varje webbplats skalning eller inte</span><span class="sxs-lookup"><span data-stu-id="206ad-133">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206ad-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="206ad-134">-ResourceGroupName</span></span>
<span data-ttu-id="206ad-135">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="206ad-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206ad-136">-Tier</span><span class="sxs-lookup"><span data-stu-id="206ad-136">-Tier</span></span>
<span data-ttu-id="206ad-137">Sker</span><span class="sxs-lookup"><span data-stu-id="206ad-137">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206ad-138">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="206ad-138">-WorkerSize</span></span>
<span data-ttu-id="206ad-139">Webb arbetarens storlek</span><span class="sxs-lookup"><span data-stu-id="206ad-139">Size of web worker</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="206ad-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="206ad-140">CommonParameters</span></span>
<span data-ttu-id="206ad-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="206ad-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="206ad-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="206ad-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="206ad-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="206ad-143">INPUTS</span></span>

### <span data-ttu-id="206ad-144">Microsoft. Azure. commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="206ad-144">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="206ad-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="206ad-145">OUTPUTS</span></span>

### <span data-ttu-id="206ad-146">Microsoft. Azure. commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="206ad-146">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="206ad-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="206ad-147">NOTES</span></span>

## <span data-ttu-id="206ad-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="206ad-148">RELATED LINKS</span></span>

[<span data-ttu-id="206ad-149">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="206ad-149">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="206ad-150">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="206ad-150">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="206ad-151">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="206ad-151">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


