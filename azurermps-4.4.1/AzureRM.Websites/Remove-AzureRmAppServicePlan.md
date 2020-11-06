---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: d1d07e27a7ad6fb6059cbfc8e4c972b1cedaf7e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585247"
---
# <span data-ttu-id="2aeec-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2aeec-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="2aeec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2aeec-102">SYNOPSIS</span></span>
<span data-ttu-id="2aeec-103">Tar bort en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="2aeec-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aeec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2aeec-104">SYNTAX</span></span>

### <span data-ttu-id="2aeec-105">S</span><span class="sxs-lookup"><span data-stu-id="2aeec-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aeec-106">S2</span><span class="sxs-lookup"><span data-stu-id="2aeec-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aeec-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2aeec-107">DESCRIPTION</span></span>
<span data-ttu-id="2aeec-108">Cmdleten **Remove-AzureRmAppServicePlan** tar bort en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="2aeec-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="2aeec-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2aeec-109">EXAMPLES</span></span>

### <span data-ttu-id="2aeec-110">Exempel 1: ta bort en app service-plan</span><span class="sxs-lookup"><span data-stu-id="2aeec-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="2aeec-111">Det här kommandot tar bort Azure App Service-planen med namnet ContosoASP som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="2aeec-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2aeec-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2aeec-112">PARAMETERS</span></span>

### <span data-ttu-id="2aeec-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2aeec-113">-AppServicePlan</span></span>
<span data-ttu-id="2aeec-114">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="2aeec-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="2aeec-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2aeec-115">-Force</span></span>
<span data-ttu-id="2aeec-116">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="2aeec-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="2aeec-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2aeec-117">-Name</span></span>
<span data-ttu-id="2aeec-118">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="2aeec-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="2aeec-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aeec-119">-ResourceGroupName</span></span>
<span data-ttu-id="2aeec-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2aeec-120">Resource Group Name</span></span>

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

### <span data-ttu-id="2aeec-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2aeec-121">-Confirm</span></span>
<span data-ttu-id="2aeec-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2aeec-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aeec-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aeec-123">-WhatIf</span></span>
<span data-ttu-id="2aeec-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2aeec-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aeec-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2aeec-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aeec-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aeec-126">-DefaultProfile</span></span>
<span data-ttu-id="2aeec-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2aeec-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aeec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aeec-128">CommonParameters</span></span>
<span data-ttu-id="2aeec-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aeec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aeec-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aeec-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aeec-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2aeec-131">INPUTS</span></span>

### <span data-ttu-id="2aeec-132">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="2aeec-132">ServerFarmWithRichSku</span></span>
<span data-ttu-id="2aeec-133">Parametern ' AppServicePlan ' godkänner värdet av typen ' ServerFarmWithRichSku ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2aeec-133">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="2aeec-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2aeec-134">OUTPUTS</span></span>

### <span data-ttu-id="2aeec-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2aeec-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="2aeec-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2aeec-136">NOTES</span></span>

## <span data-ttu-id="2aeec-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2aeec-137">RELATED LINKS</span></span>

[<span data-ttu-id="2aeec-138">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2aeec-138">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="2aeec-139">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2aeec-139">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="2aeec-140">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2aeec-140">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


