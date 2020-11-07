---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: 09491e82a1eb0ab6b77a382fc727d385bbd6820f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757168"
---
# <span data-ttu-id="735a2-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="735a2-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="735a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="735a2-102">SYNOPSIS</span></span>
<span data-ttu-id="735a2-103">Skapar en Azure App Service-plan på en given Geo-plats.</span><span class="sxs-lookup"><span data-stu-id="735a2-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="735a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="735a2-104">SYNTAX</span></span>

### <span data-ttu-id="735a2-105">S</span><span class="sxs-lookup"><span data-stu-id="735a2-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob][-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="735a2-106">S2</span><span class="sxs-lookup"><span data-stu-id="735a2-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="735a2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="735a2-107">DESCRIPTION</span></span>
<span data-ttu-id="735a2-108">Cmdleten **New-AzureRmAppServicePlan** skapar en Azure App Service-plan på en given Geo-plats med den angivna nivån, arbetarens arbets storlek och antalet arbetare.</span><span class="sxs-lookup"><span data-stu-id="735a2-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="735a2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="735a2-109">EXAMPLES</span></span>

### <span data-ttu-id="735a2-110">Exempel 1: skapa en app service-plan</span><span class="sxs-lookup"><span data-stu-id="735a2-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="735a2-111">Det här kommandot skapar en app service-plan med namnet ContosoASP i resurs gruppen som heter default-West-väst på Geo-platsen.</span><span class="sxs-lookup"><span data-stu-id="735a2-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="735a2-112">Kommandot anger en enkel nivå och tilldelar två små arbets tagare.</span><span class="sxs-lookup"><span data-stu-id="735a2-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="735a2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="735a2-113">PARAMETERS</span></span>

### <span data-ttu-id="735a2-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="735a2-114">-AppServicePlan</span></span>
<span data-ttu-id="735a2-115">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="735a2-115">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="735a2-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="735a2-116">-AseName</span></span>
<span data-ttu-id="735a2-117">App Service Environment</span><span class="sxs-lookup"><span data-stu-id="735a2-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735a2-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="735a2-118">-AseResourceGroupName</span></span>
<span data-ttu-id="735a2-119">App Service Environment resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="735a2-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735a2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735a2-120">-DefaultProfile</span></span>
<span data-ttu-id="735a2-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="735a2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735a2-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="735a2-122">-Location</span></span>
<span data-ttu-id="735a2-123">Plats</span><span class="sxs-lookup"><span data-stu-id="735a2-123">Location</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735a2-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="735a2-124">-Name</span></span>
<span data-ttu-id="735a2-125">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="735a2-125">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735a2-126">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="735a2-126">-NumberofWorkers</span></span>
<span data-ttu-id="735a2-127">Antal arbetare</span><span class="sxs-lookup"><span data-stu-id="735a2-127">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735a2-128">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="735a2-128">-PerSiteScaling</span></span>
<span data-ttu-id="735a2-129">Om du vill aktivera varje webbplats skalning eller inte</span><span class="sxs-lookup"><span data-stu-id="735a2-129">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735a2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="735a2-130">-ResourceGroupName</span></span>
<span data-ttu-id="735a2-131">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="735a2-131">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735a2-132">-Tier</span><span class="sxs-lookup"><span data-stu-id="735a2-132">-Tier</span></span>
<span data-ttu-id="735a2-133">Sker</span><span class="sxs-lookup"><span data-stu-id="735a2-133">Tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735a2-134">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="735a2-134">-WorkerSize</span></span>
<span data-ttu-id="735a2-135">Webb arbetarens storlek</span><span class="sxs-lookup"><span data-stu-id="735a2-135">Size of web worker</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="735a2-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="735a2-136">-AsJob</span></span>
<span data-ttu-id="735a2-137">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="735a2-137">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735a2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735a2-138">CommonParameters</span></span>
<span data-ttu-id="735a2-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="735a2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735a2-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="735a2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735a2-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="735a2-141">INPUTS</span></span>

### <span data-ttu-id="735a2-142">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="735a2-142">ServerFarmWithRichSku</span></span>
<span data-ttu-id="735a2-143">Parametern ' AppServicePlan ' godkänner värdet av typen ' ServerFarmWithRichSku ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="735a2-143">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="735a2-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="735a2-144">OUTPUTS</span></span>

### <span data-ttu-id="735a2-145">Microsoft. Azure. Management. webbplatser. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="735a2-145">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="735a2-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="735a2-146">NOTES</span></span>

## <span data-ttu-id="735a2-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="735a2-147">RELATED LINKS</span></span>

[<span data-ttu-id="735a2-148">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="735a2-148">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="735a2-149">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="735a2-149">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="735a2-150">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="735a2-150">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


