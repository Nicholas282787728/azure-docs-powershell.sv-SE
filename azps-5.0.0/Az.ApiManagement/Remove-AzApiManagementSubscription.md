---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 8c6bc7a9e29d6f187285cacdc9df3621fcba8d0f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324023"
---
# <span data-ttu-id="67a63-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="67a63-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="67a63-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67a63-102">SYNOPSIS</span></span>
<span data-ttu-id="67a63-103">Tar bort ett befintligt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="67a63-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="67a63-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67a63-104">SYNTAX</span></span>

### <span data-ttu-id="67a63-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="67a63-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67a63-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="67a63-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67a63-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="67a63-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67a63-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67a63-108">DESCRIPTION</span></span>
<span data-ttu-id="67a63-109">Cmdleten **Remove-AzApiManagementSubscription** tar bort en befintlig prenumeration.</span><span class="sxs-lookup"><span data-stu-id="67a63-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="67a63-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67a63-110">EXAMPLES</span></span>

### <span data-ttu-id="67a63-111">Exempel 1: ta bort ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="67a63-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="67a63-112">Det här kommandot tar bort ett befintligt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="67a63-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="67a63-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67a63-113">PARAMETERS</span></span>

### <span data-ttu-id="67a63-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="67a63-114">-Context</span></span>
<span data-ttu-id="67a63-115">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="67a63-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="67a63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a63-116">-DefaultProfile</span></span>
<span data-ttu-id="67a63-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67a63-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67a63-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67a63-118">-InputObject</span></span>
<span data-ttu-id="67a63-119">Instans av PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="67a63-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="67a63-120">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="67a63-120">This parameter is required.</span></span>

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

### <span data-ttu-id="67a63-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67a63-121">-PassThru</span></span>
<span data-ttu-id="67a63-122">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller ett $false värde.</span><span class="sxs-lookup"><span data-stu-id="67a63-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="67a63-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67a63-123">-ResourceId</span></span>
<span data-ttu-id="67a63-124">Prenumeration på arm-ResourceId.</span><span class="sxs-lookup"><span data-stu-id="67a63-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="67a63-125">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="67a63-125">This parameter is required.</span></span>

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

### <span data-ttu-id="67a63-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67a63-126">-SubscriptionId</span></span>
<span data-ttu-id="67a63-127">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="67a63-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="67a63-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="67a63-128">-Confirm</span></span>
<span data-ttu-id="67a63-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="67a63-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67a63-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67a63-130">-WhatIf</span></span>
<span data-ttu-id="67a63-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="67a63-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67a63-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="67a63-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67a63-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a63-133">CommonParameters</span></span>
<span data-ttu-id="67a63-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67a63-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a63-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67a63-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a63-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67a63-136">INPUTS</span></span>

### <span data-ttu-id="67a63-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="67a63-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="67a63-138">System. String</span><span class="sxs-lookup"><span data-stu-id="67a63-138">System.String</span></span>

### <span data-ttu-id="67a63-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="67a63-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="67a63-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67a63-140">OUTPUTS</span></span>

### <span data-ttu-id="67a63-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67a63-141">System.Boolean</span></span>

## <span data-ttu-id="67a63-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67a63-142">NOTES</span></span>

## <span data-ttu-id="67a63-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67a63-143">RELATED LINKS</span></span>

[<span data-ttu-id="67a63-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="67a63-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="67a63-145">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="67a63-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="67a63-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="67a63-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


