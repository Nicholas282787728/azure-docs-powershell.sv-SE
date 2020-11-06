---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d5164e47dd759538fea6f0ab143ef9640055f1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575412"
---
# <span data-ttu-id="4d077-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4d077-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="4d077-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d077-102">SYNOPSIS</span></span>
<span data-ttu-id="4d077-103">Tar bort en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="4d077-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d077-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d077-104">SYNTAX</span></span>

### <span data-ttu-id="4d077-105">S</span><span class="sxs-lookup"><span data-stu-id="4d077-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d077-106">S2</span><span class="sxs-lookup"><span data-stu-id="4d077-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d077-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d077-107">DESCRIPTION</span></span>
<span data-ttu-id="4d077-108">Cmdleten **Remove-AzureRmAppServicePlan** tar bort en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="4d077-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="4d077-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d077-109">EXAMPLES</span></span>

### <span data-ttu-id="4d077-110">Exempel 1: ta bort en app service-plan</span><span class="sxs-lookup"><span data-stu-id="4d077-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="4d077-111">Det här kommandot tar bort Azure App Service-planen med namnet ContosoASP som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="4d077-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="4d077-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d077-112">PARAMETERS</span></span>

### <span data-ttu-id="4d077-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4d077-113">-AppServicePlan</span></span>
<span data-ttu-id="4d077-114">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="4d077-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="4d077-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d077-115">-DefaultProfile</span></span>
<span data-ttu-id="4d077-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d077-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d077-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4d077-117">-Force</span></span>
<span data-ttu-id="4d077-118">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="4d077-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="4d077-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d077-119">-Name</span></span>
<span data-ttu-id="4d077-120">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="4d077-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="4d077-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d077-121">-ResourceGroupName</span></span>
<span data-ttu-id="4d077-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="4d077-122">Resource Group Name</span></span>

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

### <span data-ttu-id="4d077-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d077-123">-Confirm</span></span>
<span data-ttu-id="4d077-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d077-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d077-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d077-125">-WhatIf</span></span>
<span data-ttu-id="4d077-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d077-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d077-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d077-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d077-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d077-128">-AsJob</span></span>
<span data-ttu-id="4d077-129">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4d077-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d077-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d077-130">CommonParameters</span></span>
<span data-ttu-id="4d077-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d077-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d077-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d077-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d077-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d077-133">INPUTS</span></span>

### <span data-ttu-id="4d077-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="4d077-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="4d077-135">Parametern ' AppServicePlan ' godkänner värdet av typen ' ServerFarmWithRichSku ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4d077-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="4d077-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d077-136">OUTPUTS</span></span>

### <span data-ttu-id="4d077-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4d077-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="4d077-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d077-138">NOTES</span></span>

## <span data-ttu-id="4d077-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d077-139">RELATED LINKS</span></span>

[<span data-ttu-id="4d077-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4d077-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="4d077-141">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4d077-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="4d077-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4d077-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


