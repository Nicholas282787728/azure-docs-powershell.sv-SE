---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: eac153c22a576686feb15b75f3180ed4fb12ec94
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930766"
---
# <span data-ttu-id="968f8-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="968f8-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="968f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="968f8-102">SYNOPSIS</span></span>
<span data-ttu-id="968f8-103">Ställer in en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="968f8-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="968f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="968f8-104">SYNTAX</span></span>

### <span data-ttu-id="968f8-105">S</span><span class="sxs-lookup"><span data-stu-id="968f8-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="968f8-106">S2</span><span class="sxs-lookup"><span data-stu-id="968f8-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="968f8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="968f8-107">DESCRIPTION</span></span>
<span data-ttu-id="968f8-108">Cmdleten **set-AzureRmAppServicePlan** anger en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="968f8-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="968f8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="968f8-109">EXAMPLES</span></span>

### <span data-ttu-id="968f8-110">1: ändra en app service-plan</span><span class="sxs-lookup"><span data-stu-id="968f8-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="968f8-111">Det här kommandot anger alternativet PerSiteScaling till true i App Service-planen med namnet ContosoASP som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="968f8-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="968f8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="968f8-112">PARAMETERS</span></span>

### <span data-ttu-id="968f8-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="968f8-113">-AdminSiteName</span></span>
<span data-ttu-id="968f8-114">Namn på administratörs webbplats</span><span class="sxs-lookup"><span data-stu-id="968f8-114">Admin Site Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="968f8-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="968f8-115">-AppServicePlan</span></span>
<span data-ttu-id="968f8-116">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="968f8-116">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="968f8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="968f8-117">-DefaultProfile</span></span>
<span data-ttu-id="968f8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="968f8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="968f8-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="968f8-119">-Name</span></span>
<span data-ttu-id="968f8-120">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="968f8-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="968f8-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="968f8-121">-NumberofWorkers</span></span>
<span data-ttu-id="968f8-122">Antal arbetare</span><span class="sxs-lookup"><span data-stu-id="968f8-122">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="968f8-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="968f8-123">-PerSiteScaling</span></span>
<span data-ttu-id="968f8-124">Skalning för varje webbplats</span><span class="sxs-lookup"><span data-stu-id="968f8-124">Per Site Scaling Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="968f8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="968f8-125">-ResourceGroupName</span></span>
<span data-ttu-id="968f8-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="968f8-126">Resource Group Name</span></span>

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

### <span data-ttu-id="968f8-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="968f8-127">-Tier</span></span>
<span data-ttu-id="968f8-128">Sker</span><span class="sxs-lookup"><span data-stu-id="968f8-128">Tier</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="968f8-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="968f8-129">-WorkerSize</span></span>
<span data-ttu-id="968f8-130">Arbetarens storlek</span><span class="sxs-lookup"><span data-stu-id="968f8-130">Worker Size</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="968f8-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="968f8-131">-AsJob</span></span>
<span data-ttu-id="968f8-132">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="968f8-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="968f8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="968f8-133">CommonParameters</span></span>
<span data-ttu-id="968f8-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="968f8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="968f8-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="968f8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="968f8-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="968f8-136">INPUTS</span></span>

### <span data-ttu-id="968f8-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="968f8-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="968f8-138">Parametern ' AppServicePlan ' godkänner värdet av typen ' ServerFarmWithRichSku ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="968f8-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="968f8-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="968f8-139">OUTPUTS</span></span>

### <span data-ttu-id="968f8-140">Microsoft. Azure. Management. webbplatser. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="968f8-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="968f8-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="968f8-141">NOTES</span></span>

## <span data-ttu-id="968f8-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="968f8-142">RELATED LINKS</span></span>

[<span data-ttu-id="968f8-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="968f8-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="968f8-144">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="968f8-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="968f8-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="968f8-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="968f8-146">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="968f8-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="968f8-147">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="968f8-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="968f8-148">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="968f8-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


