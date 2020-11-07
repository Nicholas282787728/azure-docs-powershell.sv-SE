---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 411fa67d81b772c2e9dcd6b1690e8eac50de3ea0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917745"
---
# <span data-ttu-id="851fa-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="851fa-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="851fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="851fa-102">SYNOPSIS</span></span>
<span data-ttu-id="851fa-103">Tar bort ett befintligt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="851fa-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="851fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="851fa-104">SYNTAX</span></span>

```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="851fa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="851fa-105">DESCRIPTION</span></span>
<span data-ttu-id="851fa-106">Cmdleten **Remove-AzApiManagementSubscription** tar bort en befintlig prenumeration.</span><span class="sxs-lookup"><span data-stu-id="851fa-106">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="851fa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="851fa-107">EXAMPLES</span></span>

### <span data-ttu-id="851fa-108">Exempel 1: ta bort ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="851fa-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="851fa-109">Det här kommandot tar bort ett befintligt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="851fa-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="851fa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="851fa-110">PARAMETERS</span></span>

### <span data-ttu-id="851fa-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="851fa-111">-Context</span></span>
<span data-ttu-id="851fa-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="851fa-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="851fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="851fa-113">-DefaultProfile</span></span>
<span data-ttu-id="851fa-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="851fa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="851fa-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="851fa-115">-PassThru</span></span>
<span data-ttu-id="851fa-116">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller ett $false värde.</span><span class="sxs-lookup"><span data-stu-id="851fa-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="851fa-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="851fa-117">-SubscriptionId</span></span>
<span data-ttu-id="851fa-118">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="851fa-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="851fa-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="851fa-119">-Confirm</span></span>
<span data-ttu-id="851fa-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="851fa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="851fa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="851fa-121">-WhatIf</span></span>
<span data-ttu-id="851fa-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="851fa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="851fa-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="851fa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="851fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="851fa-124">CommonParameters</span></span>
<span data-ttu-id="851fa-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="851fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="851fa-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="851fa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="851fa-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="851fa-127">INPUTS</span></span>

### <span data-ttu-id="851fa-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="851fa-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="851fa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="851fa-129">System.String</span></span>

### <span data-ttu-id="851fa-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="851fa-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="851fa-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="851fa-131">OUTPUTS</span></span>

### <span data-ttu-id="851fa-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="851fa-132">System.Boolean</span></span>

## <span data-ttu-id="851fa-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="851fa-133">NOTES</span></span>

## <span data-ttu-id="851fa-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="851fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="851fa-135">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="851fa-135">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="851fa-136">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="851fa-136">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="851fa-137">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="851fa-137">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


