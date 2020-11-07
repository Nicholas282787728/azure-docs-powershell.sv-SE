---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: b679b98e84f389e35e7dc291822049e554d40a9a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923261"
---
# <span data-ttu-id="3812e-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3812e-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="3812e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3812e-102">SYNOPSIS</span></span>
<span data-ttu-id="3812e-103">Ställer in en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="3812e-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="3812e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3812e-104">SYNTAX</span></span>

### <span data-ttu-id="3812e-105">S</span><span class="sxs-lookup"><span data-stu-id="3812e-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3812e-106">S2</span><span class="sxs-lookup"><span data-stu-id="3812e-106">S2</span></span>
```
Set-AzAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3812e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3812e-107">DESCRIPTION</span></span>
<span data-ttu-id="3812e-108">Cmdleten **set-AzAppServicePlan** anger en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="3812e-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="3812e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3812e-109">EXAMPLES</span></span>

### <span data-ttu-id="3812e-110">1: ändra en app service-plan</span><span class="sxs-lookup"><span data-stu-id="3812e-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="3812e-111">Det här kommandot anger alternativet PerSiteScaling till true i App Service-planen med namnet ContosoASP som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="3812e-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3812e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3812e-112">PARAMETERS</span></span>

### <span data-ttu-id="3812e-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="3812e-113">-AdminSiteName</span></span>
<span data-ttu-id="3812e-114">Namn på administratörs webbplats</span><span class="sxs-lookup"><span data-stu-id="3812e-114">Admin Site Name</span></span>

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

### <span data-ttu-id="3812e-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3812e-115">-AppServicePlan</span></span>
<span data-ttu-id="3812e-116">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="3812e-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="3812e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3812e-117">-DefaultProfile</span></span>
<span data-ttu-id="3812e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3812e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3812e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="3812e-119">-Name</span></span>
<span data-ttu-id="3812e-120">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="3812e-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="3812e-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="3812e-121">-NumberofWorkers</span></span>
<span data-ttu-id="3812e-122">Antal arbetare</span><span class="sxs-lookup"><span data-stu-id="3812e-122">Number Of Workers</span></span>

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

### <span data-ttu-id="3812e-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="3812e-123">-PerSiteScaling</span></span>
<span data-ttu-id="3812e-124">Skalning för varje webbplats</span><span class="sxs-lookup"><span data-stu-id="3812e-124">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="3812e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3812e-125">-ResourceGroupName</span></span>
<span data-ttu-id="3812e-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="3812e-126">Resource Group Name</span></span>

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

### <span data-ttu-id="3812e-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="3812e-127">-Tier</span></span>
<span data-ttu-id="3812e-128">Sker</span><span class="sxs-lookup"><span data-stu-id="3812e-128">Tier</span></span>

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

### <span data-ttu-id="3812e-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="3812e-129">-WorkerSize</span></span>
<span data-ttu-id="3812e-130">Arbetarens storlek</span><span class="sxs-lookup"><span data-stu-id="3812e-130">Worker Size</span></span>

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
### <span data-ttu-id="3812e-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3812e-131">-AsJob</span></span>
<span data-ttu-id="3812e-132">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3812e-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3812e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3812e-133">CommonParameters</span></span>
<span data-ttu-id="3812e-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3812e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3812e-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3812e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3812e-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3812e-136">INPUTS</span></span>

### <span data-ttu-id="3812e-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="3812e-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="3812e-138">Parametern ' AppServicePlan ' godkänner värdet av typen ' ServerFarmWithRichSku ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3812e-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="3812e-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3812e-139">OUTPUTS</span></span>

### <span data-ttu-id="3812e-140">Microsoft. Azure. Management. webbplatser. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="3812e-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="3812e-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3812e-141">NOTES</span></span>

## <span data-ttu-id="3812e-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3812e-142">RELATED LINKS</span></span>

[<span data-ttu-id="3812e-143">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3812e-143">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="3812e-144">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3812e-144">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="3812e-145">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3812e-145">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="3812e-146">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3812e-146">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="3812e-147">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3812e-147">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="3812e-148">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3812e-148">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


