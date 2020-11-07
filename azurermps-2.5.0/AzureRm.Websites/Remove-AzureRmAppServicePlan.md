---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: e8ce0397a59a72e2960a8e0af978c1b5484c53af
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928642"
---
# <span data-ttu-id="5ad3f-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5ad3f-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="5ad3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ad3f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ad3f-103">Tar bort en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="5ad3f-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ad3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ad3f-104">SYNTAX</span></span>

### <span data-ttu-id="5ad3f-105">S</span><span class="sxs-lookup"><span data-stu-id="5ad3f-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ad3f-106">S2</span><span class="sxs-lookup"><span data-stu-id="5ad3f-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ad3f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ad3f-107">DESCRIPTION</span></span>
<span data-ttu-id="5ad3f-108">Cmdleten **Remove-AzureRmAppServicePlan** tar bort en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="5ad3f-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="5ad3f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ad3f-109">EXAMPLES</span></span>

### <span data-ttu-id="5ad3f-110">Exempel 1: ta bort en app service-plan</span><span class="sxs-lookup"><span data-stu-id="5ad3f-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="5ad3f-111">Det här kommandot tar bort Azure App Service-planen med namnet ContosoASP som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="5ad3f-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="5ad3f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ad3f-112">PARAMETERS</span></span>

### <span data-ttu-id="5ad3f-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5ad3f-113">-AppServicePlan</span></span>
<span data-ttu-id="5ad3f-114">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="5ad3f-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="5ad3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ad3f-115">-DefaultProfile</span></span>
<span data-ttu-id="5ad3f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ad3f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ad3f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5ad3f-117">-Force</span></span>
<span data-ttu-id="5ad3f-118">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="5ad3f-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="5ad3f-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ad3f-119">-Name</span></span>
<span data-ttu-id="5ad3f-120">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="5ad3f-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="5ad3f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ad3f-121">-ResourceGroupName</span></span>
<span data-ttu-id="5ad3f-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5ad3f-122">Resource Group Name</span></span>

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

### <span data-ttu-id="5ad3f-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ad3f-123">-Confirm</span></span>
<span data-ttu-id="5ad3f-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ad3f-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad3f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ad3f-125">-WhatIf</span></span>
<span data-ttu-id="5ad3f-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ad3f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ad3f-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ad3f-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad3f-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ad3f-128">-AsJob</span></span>
<span data-ttu-id="5ad3f-129">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5ad3f-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ad3f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ad3f-130">CommonParameters</span></span>
<span data-ttu-id="5ad3f-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ad3f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ad3f-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ad3f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ad3f-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ad3f-133">INPUTS</span></span>

### <span data-ttu-id="5ad3f-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="5ad3f-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="5ad3f-135">Parametern ' AppServicePlan ' godkänner värdet av typen ' ServerFarmWithRichSku ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5ad3f-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="5ad3f-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ad3f-136">OUTPUTS</span></span>

### <span data-ttu-id="5ad3f-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5ad3f-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="5ad3f-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ad3f-138">NOTES</span></span>

## <span data-ttu-id="5ad3f-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ad3f-139">RELATED LINKS</span></span>

[<span data-ttu-id="5ad3f-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5ad3f-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="5ad3f-141">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5ad3f-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="5ad3f-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5ad3f-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


