---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: dfd2cfd20ab11e2e70e03dc3e166c83729ef344a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272491"
---
# <span data-ttu-id="2547d-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2547d-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="2547d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2547d-102">SYNOPSIS</span></span>
<span data-ttu-id="2547d-103">Tar bort en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="2547d-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="2547d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2547d-104">SYNTAX</span></span>

### <span data-ttu-id="2547d-105">S</span><span class="sxs-lookup"><span data-stu-id="2547d-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2547d-106">S2</span><span class="sxs-lookup"><span data-stu-id="2547d-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2547d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2547d-107">DESCRIPTION</span></span>
<span data-ttu-id="2547d-108">Cmdleten **Remove-AzAppServicePlan** tar bort en Azure App Service-plan.</span><span class="sxs-lookup"><span data-stu-id="2547d-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="2547d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2547d-109">EXAMPLES</span></span>

### <span data-ttu-id="2547d-110">Exempel 1: ta bort en app service-plan</span><span class="sxs-lookup"><span data-stu-id="2547d-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="2547d-111">Det här kommandot tar bort Azure App Service-planen med namnet ContosoASP som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="2547d-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2547d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2547d-112">PARAMETERS</span></span>

### <span data-ttu-id="2547d-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2547d-113">-AppServicePlan</span></span>
<span data-ttu-id="2547d-114">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="2547d-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="2547d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2547d-115">-AsJob</span></span>
<span data-ttu-id="2547d-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2547d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2547d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2547d-117">-DefaultProfile</span></span>
<span data-ttu-id="2547d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2547d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2547d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2547d-119">-Force</span></span>
<span data-ttu-id="2547d-120">Framtvinga borttagnings alternativ</span><span class="sxs-lookup"><span data-stu-id="2547d-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="2547d-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="2547d-121">-Name</span></span>
<span data-ttu-id="2547d-122">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="2547d-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="2547d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2547d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2547d-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2547d-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2547d-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2547d-125">-Confirm</span></span>
<span data-ttu-id="2547d-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2547d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2547d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2547d-127">-WhatIf</span></span>
<span data-ttu-id="2547d-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2547d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2547d-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2547d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2547d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2547d-130">CommonParameters</span></span>
<span data-ttu-id="2547d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2547d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2547d-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2547d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2547d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2547d-133">INPUTS</span></span>

### <span data-ttu-id="2547d-134">Microsoft. Azure. commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2547d-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="2547d-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2547d-135">OUTPUTS</span></span>

### <span data-ttu-id="2547d-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2547d-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="2547d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2547d-137">NOTES</span></span>

## <span data-ttu-id="2547d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2547d-138">RELATED LINKS</span></span>

[<span data-ttu-id="2547d-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2547d-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="2547d-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2547d-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="2547d-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2547d-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


