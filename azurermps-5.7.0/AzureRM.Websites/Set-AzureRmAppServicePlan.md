---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 16b2c8df737047619366ebf6b75a4c2ed2264fdc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581863"
---
# <span data-ttu-id="4fbc5-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4fbc5-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="4fbc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4fbc5-102">SYNOPSIS</span></span>
<span data-ttu-id="4fbc5-103">Ställer in en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="4fbc5-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fbc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4fbc5-104">SYNTAX</span></span>

### <span data-ttu-id="4fbc5-105">S</span><span class="sxs-lookup"><span data-stu-id="4fbc5-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fbc5-106">S2</span><span class="sxs-lookup"><span data-stu-id="4fbc5-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4fbc5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4fbc5-107">DESCRIPTION</span></span>
<span data-ttu-id="4fbc5-108">Cmdleten **set-AzureRmAppServicePlan** anger en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="4fbc5-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="4fbc5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4fbc5-109">EXAMPLES</span></span>

### <span data-ttu-id="4fbc5-110">1: ändra en app service-plan</span><span class="sxs-lookup"><span data-stu-id="4fbc5-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="4fbc5-111">Det här kommandot anger alternativet PerSiteScaling till true i App Service-planen med namnet ContosoASP som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="4fbc5-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="4fbc5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4fbc5-112">PARAMETERS</span></span>

### <span data-ttu-id="4fbc5-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="4fbc5-113">-AdminSiteName</span></span>
<span data-ttu-id="4fbc5-114">Namn på administratörs webbplats</span><span class="sxs-lookup"><span data-stu-id="4fbc5-114">Admin Site Name</span></span>

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

### <span data-ttu-id="4fbc5-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4fbc5-115">-AppServicePlan</span></span>
<span data-ttu-id="4fbc5-116">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="4fbc5-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="4fbc5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fbc5-117">-DefaultProfile</span></span>
<span data-ttu-id="4fbc5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4fbc5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fbc5-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="4fbc5-119">-Name</span></span>
<span data-ttu-id="4fbc5-120">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="4fbc5-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="4fbc5-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="4fbc5-121">-NumberofWorkers</span></span>
<span data-ttu-id="4fbc5-122">Antal arbetare</span><span class="sxs-lookup"><span data-stu-id="4fbc5-122">Number Of Workers</span></span>

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

### <span data-ttu-id="4fbc5-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="4fbc5-123">-PerSiteScaling</span></span>
<span data-ttu-id="4fbc5-124">Skalning för varje webbplats</span><span class="sxs-lookup"><span data-stu-id="4fbc5-124">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="4fbc5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fbc5-125">-ResourceGroupName</span></span>
<span data-ttu-id="4fbc5-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="4fbc5-126">Resource Group Name</span></span>

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

### <span data-ttu-id="4fbc5-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="4fbc5-127">-Tier</span></span>
<span data-ttu-id="4fbc5-128">Sker</span><span class="sxs-lookup"><span data-stu-id="4fbc5-128">Tier</span></span>

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

### <span data-ttu-id="4fbc5-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="4fbc5-129">-WorkerSize</span></span>
<span data-ttu-id="4fbc5-130">Arbetarens storlek</span><span class="sxs-lookup"><span data-stu-id="4fbc5-130">Worker Size</span></span>

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
### <span data-ttu-id="4fbc5-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fbc5-131">-AsJob</span></span>
<span data-ttu-id="4fbc5-132">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4fbc5-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4fbc5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fbc5-133">CommonParameters</span></span>
<span data-ttu-id="4fbc5-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fbc5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fbc5-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fbc5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fbc5-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4fbc5-136">INPUTS</span></span>

### <span data-ttu-id="4fbc5-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="4fbc5-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="4fbc5-138">Parametern ' AppServicePlan ' godkänner värdet av typen ' ServerFarmWithRichSku ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4fbc5-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="4fbc5-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4fbc5-139">OUTPUTS</span></span>

### <span data-ttu-id="4fbc5-140">Microsoft. Azure. Management. webbplatser. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="4fbc5-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="4fbc5-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4fbc5-141">NOTES</span></span>

## <span data-ttu-id="4fbc5-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4fbc5-142">RELATED LINKS</span></span>

[<span data-ttu-id="4fbc5-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4fbc5-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="4fbc5-144">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4fbc5-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="4fbc5-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4fbc5-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="4fbc5-146">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4fbc5-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="4fbc5-147">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4fbc5-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="4fbc5-148">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4fbc5-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


