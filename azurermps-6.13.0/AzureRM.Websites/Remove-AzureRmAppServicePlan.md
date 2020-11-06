---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: b97506b8f104859c54c55ee1a937916623f4201d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573820"
---
# <span data-ttu-id="85aea-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="85aea-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="85aea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85aea-102">SYNOPSIS</span></span>
<span data-ttu-id="85aea-103">Tar bort en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="85aea-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85aea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85aea-104">SYNTAX</span></span>

### <span data-ttu-id="85aea-105">S</span><span class="sxs-lookup"><span data-stu-id="85aea-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85aea-106">S2</span><span class="sxs-lookup"><span data-stu-id="85aea-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85aea-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85aea-107">DESCRIPTION</span></span>
<span data-ttu-id="85aea-108">Cmdleten **Remove-AzureRmAppServicePlan** tar bort en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="85aea-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="85aea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85aea-109">EXAMPLES</span></span>

### <span data-ttu-id="85aea-110">Exempel 1: ta bort en app service-plan</span><span class="sxs-lookup"><span data-stu-id="85aea-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="85aea-111">Det här kommandot tar bort Azure App Service-planen med namnet ContosoASP som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="85aea-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="85aea-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85aea-112">PARAMETERS</span></span>

### <span data-ttu-id="85aea-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="85aea-113">-AppServicePlan</span></span>
<span data-ttu-id="85aea-114">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="85aea-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="85aea-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85aea-115">-AsJob</span></span>
<span data-ttu-id="85aea-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="85aea-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85aea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85aea-117">-DefaultProfile</span></span>
<span data-ttu-id="85aea-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="85aea-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85aea-119">-Force</span><span class="sxs-lookup"><span data-stu-id="85aea-119">-Force</span></span>
<span data-ttu-id="85aea-120">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="85aea-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="85aea-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="85aea-121">-Name</span></span>
<span data-ttu-id="85aea-122">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="85aea-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="85aea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85aea-123">-ResourceGroupName</span></span>
<span data-ttu-id="85aea-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="85aea-124">Resource Group Name</span></span>

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

### <span data-ttu-id="85aea-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="85aea-125">-Confirm</span></span>
<span data-ttu-id="85aea-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="85aea-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85aea-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85aea-127">-WhatIf</span></span>
<span data-ttu-id="85aea-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="85aea-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85aea-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="85aea-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85aea-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85aea-130">CommonParameters</span></span>
<span data-ttu-id="85aea-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85aea-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85aea-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85aea-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85aea-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85aea-133">INPUTS</span></span>

### <span data-ttu-id="85aea-134">Microsoft. Azure. Management. webbplatser. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="85aea-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="85aea-135">Parametrar: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="85aea-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="85aea-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85aea-136">OUTPUTS</span></span>

### <span data-ttu-id="85aea-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="85aea-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="85aea-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85aea-138">NOTES</span></span>

## <span data-ttu-id="85aea-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85aea-139">RELATED LINKS</span></span>

[<span data-ttu-id="85aea-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="85aea-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="85aea-141">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="85aea-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="85aea-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="85aea-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


