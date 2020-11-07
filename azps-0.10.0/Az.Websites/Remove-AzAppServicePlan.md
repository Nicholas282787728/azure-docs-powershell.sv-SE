---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: 3d0e3ad30df71700eb83938181ed86a97a77528a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923302"
---
# <span data-ttu-id="293ef-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="293ef-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="293ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="293ef-102">SYNOPSIS</span></span>
<span data-ttu-id="293ef-103">Tar bort en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="293ef-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="293ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="293ef-104">SYNTAX</span></span>

### <span data-ttu-id="293ef-105">S</span><span class="sxs-lookup"><span data-stu-id="293ef-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="293ef-106">S2</span><span class="sxs-lookup"><span data-stu-id="293ef-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AppServicePlan] <AppServicePlan> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="293ef-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="293ef-107">DESCRIPTION</span></span>
<span data-ttu-id="293ef-108">Cmdleten **Remove-AzAppServicePlan** tar bort en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="293ef-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="293ef-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="293ef-109">EXAMPLES</span></span>

### <span data-ttu-id="293ef-110">Exempel 1: ta bort en app service-plan</span><span class="sxs-lookup"><span data-stu-id="293ef-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="293ef-111">Det här kommandot tar bort Azure App Service-planen med namnet ContosoASP som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="293ef-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="293ef-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="293ef-112">PARAMETERS</span></span>

### <span data-ttu-id="293ef-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="293ef-113">-AppServicePlan</span></span>
<span data-ttu-id="293ef-114">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="293ef-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="293ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293ef-115">-DefaultProfile</span></span>
<span data-ttu-id="293ef-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="293ef-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="293ef-117">-Force</span><span class="sxs-lookup"><span data-stu-id="293ef-117">-Force</span></span>
<span data-ttu-id="293ef-118">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="293ef-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="293ef-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="293ef-119">-Name</span></span>
<span data-ttu-id="293ef-120">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="293ef-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="293ef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="293ef-121">-ResourceGroupName</span></span>
<span data-ttu-id="293ef-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="293ef-122">Resource Group Name</span></span>

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

### <span data-ttu-id="293ef-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="293ef-123">-Confirm</span></span>
<span data-ttu-id="293ef-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="293ef-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="293ef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="293ef-125">-WhatIf</span></span>
<span data-ttu-id="293ef-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="293ef-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="293ef-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="293ef-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="293ef-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="293ef-128">-AsJob</span></span>
<span data-ttu-id="293ef-129">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="293ef-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="293ef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293ef-130">CommonParameters</span></span>
<span data-ttu-id="293ef-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="293ef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293ef-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="293ef-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293ef-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="293ef-133">INPUTS</span></span>

### <span data-ttu-id="293ef-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="293ef-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="293ef-135">Parametern ' AppServicePlan ' godkänner värdet av typen ' ServerFarmWithRichSku ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="293ef-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="293ef-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="293ef-136">OUTPUTS</span></span>

### <span data-ttu-id="293ef-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="293ef-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="293ef-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="293ef-138">NOTES</span></span>

## <span data-ttu-id="293ef-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="293ef-139">RELATED LINKS</span></span>

[<span data-ttu-id="293ef-140">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="293ef-140">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="293ef-141">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="293ef-141">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="293ef-142">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="293ef-142">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


