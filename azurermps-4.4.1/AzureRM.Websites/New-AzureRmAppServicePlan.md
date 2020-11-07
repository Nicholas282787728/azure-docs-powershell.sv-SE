---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: e03e7dee6e233934216c04a44c1e100d3e26347b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757731"
---
# <span data-ttu-id="46b73-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="46b73-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="46b73-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46b73-102">SYNOPSIS</span></span>
<span data-ttu-id="46b73-103">Skapar en Azure App Service-plan på en given Geo-plats.</span><span class="sxs-lookup"><span data-stu-id="46b73-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46b73-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46b73-104">SYNTAX</span></span>

### <span data-ttu-id="46b73-105">S</span><span class="sxs-lookup"><span data-stu-id="46b73-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46b73-106">S2</span><span class="sxs-lookup"><span data-stu-id="46b73-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46b73-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46b73-107">DESCRIPTION</span></span>
<span data-ttu-id="46b73-108">Cmdleten **New-AzureRmAppServicePlan** skapar en Azure App Service-plan på en given Geo-plats med den angivna nivån, arbetarens arbets storlek och antalet arbetare.</span><span class="sxs-lookup"><span data-stu-id="46b73-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="46b73-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46b73-109">EXAMPLES</span></span>

### <span data-ttu-id="46b73-110">Exempel 1: skapa en app service-plan</span><span class="sxs-lookup"><span data-stu-id="46b73-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="46b73-111">Det här kommandot skapar en app service-plan med namnet ContosoASP i resurs gruppen som heter default-West-väst på Geo-platsen.</span><span class="sxs-lookup"><span data-stu-id="46b73-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="46b73-112">Kommandot anger en enkel nivå och tilldelar två små arbets tagare.</span><span class="sxs-lookup"><span data-stu-id="46b73-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="46b73-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46b73-113">PARAMETERS</span></span>

### <span data-ttu-id="46b73-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="46b73-114">-AppServicePlan</span></span>
<span data-ttu-id="46b73-115">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="46b73-115">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46b73-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="46b73-116">-AseName</span></span>
<span data-ttu-id="46b73-117">App Service Environment</span><span class="sxs-lookup"><span data-stu-id="46b73-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="46b73-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46b73-118">-AseResourceGroupName</span></span>
<span data-ttu-id="46b73-119">App Service Environment resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="46b73-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="46b73-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="46b73-120">-Location</span></span>
<span data-ttu-id="46b73-121">Plats</span><span class="sxs-lookup"><span data-stu-id="46b73-121">Location</span></span> 

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

### <span data-ttu-id="46b73-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="46b73-122">-Name</span></span>
<span data-ttu-id="46b73-123">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="46b73-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="46b73-124">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="46b73-124">-NumberofWorkers</span></span>
<span data-ttu-id="46b73-125">Antal arbetare</span><span class="sxs-lookup"><span data-stu-id="46b73-125">Number Of Workers</span></span>

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

### <span data-ttu-id="46b73-126">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="46b73-126">-PerSiteScaling</span></span>
<span data-ttu-id="46b73-127">Om du vill aktivera varje webbplats skalning eller inte</span><span class="sxs-lookup"><span data-stu-id="46b73-127">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="46b73-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46b73-128">-ResourceGroupName</span></span>
<span data-ttu-id="46b73-129">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="46b73-129">Resource Group Name</span></span>

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

### <span data-ttu-id="46b73-130">-Tier</span><span class="sxs-lookup"><span data-stu-id="46b73-130">-Tier</span></span>
<span data-ttu-id="46b73-131">Sker</span><span class="sxs-lookup"><span data-stu-id="46b73-131">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46b73-132">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="46b73-132">-WorkerSize</span></span>
<span data-ttu-id="46b73-133">Webb arbetarens storlek</span><span class="sxs-lookup"><span data-stu-id="46b73-133">Size of web worker</span></span>

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

### <span data-ttu-id="46b73-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b73-134">-DefaultProfile</span></span>
<span data-ttu-id="46b73-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46b73-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46b73-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b73-136">CommonParameters</span></span>
<span data-ttu-id="46b73-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b73-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b73-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46b73-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b73-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46b73-139">INPUTS</span></span>

### <span data-ttu-id="46b73-140">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="46b73-140">ServerFarmWithRichSku</span></span>
<span data-ttu-id="46b73-141">Parametern ' AppServicePlan ' godkänner värdet av typen ' ServerFarmWithRichSku ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="46b73-141">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="46b73-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46b73-142">OUTPUTS</span></span>

### <span data-ttu-id="46b73-143">Microsoft. Azure. Management. webbplatser. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="46b73-143">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="46b73-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46b73-144">NOTES</span></span>

## <span data-ttu-id="46b73-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46b73-145">RELATED LINKS</span></span>

[<span data-ttu-id="46b73-146">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="46b73-146">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="46b73-147">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="46b73-147">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="46b73-148">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="46b73-148">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


