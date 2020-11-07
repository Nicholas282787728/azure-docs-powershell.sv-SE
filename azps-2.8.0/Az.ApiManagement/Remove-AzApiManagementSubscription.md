---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 5d3ad3481a57f2578678daa88c1f3e87e9893f7c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745691"
---
# <span data-ttu-id="c41e9-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c41e9-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="c41e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c41e9-102">SYNOPSIS</span></span>
<span data-ttu-id="c41e9-103">Tar bort ett befintligt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="c41e9-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="c41e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c41e9-104">SYNTAX</span></span>

### <span data-ttu-id="c41e9-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="c41e9-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c41e9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c41e9-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c41e9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c41e9-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c41e9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c41e9-108">DESCRIPTION</span></span>
<span data-ttu-id="c41e9-109">Cmdleten **Remove-AzApiManagementSubscription** tar bort en befintlig prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c41e9-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="c41e9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c41e9-110">EXAMPLES</span></span>

### <span data-ttu-id="c41e9-111">Exempel 1: ta bort ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="c41e9-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="c41e9-112">Det här kommandot tar bort ett befintligt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="c41e9-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="c41e9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c41e9-113">PARAMETERS</span></span>

### <span data-ttu-id="c41e9-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c41e9-114">-Context</span></span>
<span data-ttu-id="c41e9-115">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c41e9-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c41e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c41e9-116">-DefaultProfile</span></span>
<span data-ttu-id="c41e9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c41e9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c41e9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c41e9-118">-InputObject</span></span>
<span data-ttu-id="c41e9-119">Instans av PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="c41e9-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="c41e9-120">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c41e9-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c41e9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c41e9-121">-PassThru</span></span>
<span data-ttu-id="c41e9-122">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller ett $false värde.</span><span class="sxs-lookup"><span data-stu-id="c41e9-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c41e9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c41e9-123">-ResourceId</span></span>
<span data-ttu-id="c41e9-124">Prenumeration på arm-ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c41e9-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="c41e9-125">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c41e9-125">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c41e9-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c41e9-126">-SubscriptionId</span></span>
<span data-ttu-id="c41e9-127">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="c41e9-127">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c41e9-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c41e9-128">-Confirm</span></span>
<span data-ttu-id="c41e9-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c41e9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c41e9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c41e9-130">-WhatIf</span></span>
<span data-ttu-id="c41e9-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c41e9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c41e9-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c41e9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c41e9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c41e9-133">CommonParameters</span></span>
<span data-ttu-id="c41e9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c41e9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c41e9-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c41e9-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c41e9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c41e9-136">INPUTS</span></span>

### <span data-ttu-id="c41e9-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c41e9-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c41e9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c41e9-138">System.String</span></span>

### <span data-ttu-id="c41e9-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c41e9-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c41e9-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c41e9-140">OUTPUTS</span></span>

### <span data-ttu-id="c41e9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c41e9-141">System.Boolean</span></span>

## <span data-ttu-id="c41e9-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c41e9-142">NOTES</span></span>

## <span data-ttu-id="c41e9-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c41e9-143">RELATED LINKS</span></span>

[<span data-ttu-id="c41e9-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c41e9-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="c41e9-145">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c41e9-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="c41e9-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c41e9-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


