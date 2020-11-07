---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 09a0af4685701de60fc85c1572b492e7582ff71e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756736"
---
# <span data-ttu-id="d5079-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d5079-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="d5079-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5079-102">SYNOPSIS</span></span>
<span data-ttu-id="d5079-103">Tar bort ett befintligt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="d5079-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5079-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5079-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5079-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5079-105">DESCRIPTION</span></span>
<span data-ttu-id="d5079-106">Cmdleten **Remove-AzureRmApiManagementSubscription** tar bort en befintlig prenumeration.</span><span class="sxs-lookup"><span data-stu-id="d5079-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="d5079-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5079-107">EXAMPLES</span></span>

### <span data-ttu-id="d5079-108">Exempel 1: ta bort ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="d5079-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="d5079-109">Det här kommandot tar bort ett befintligt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="d5079-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="d5079-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5079-110">PARAMETERS</span></span>

### <span data-ttu-id="d5079-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d5079-111">-Context</span></span>
<span data-ttu-id="d5079-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d5079-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d5079-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5079-113">-DefaultProfile</span></span>
<span data-ttu-id="d5079-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5079-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5079-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5079-115">-PassThru</span></span>
<span data-ttu-id="d5079-116">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller ett $false värde.</span><span class="sxs-lookup"><span data-stu-id="d5079-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="d5079-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5079-117">-SubscriptionId</span></span>
<span data-ttu-id="d5079-118">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="d5079-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="d5079-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d5079-119">-Confirm</span></span>
<span data-ttu-id="d5079-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d5079-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5079-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5079-121">-WhatIf</span></span>
<span data-ttu-id="d5079-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d5079-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5079-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d5079-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5079-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5079-124">CommonParameters</span></span>
<span data-ttu-id="d5079-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5079-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5079-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5079-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5079-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5079-127">INPUTS</span></span>

### <span data-ttu-id="d5079-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d5079-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d5079-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d5079-129">System.String</span></span>

### <span data-ttu-id="d5079-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d5079-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d5079-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5079-131">OUTPUTS</span></span>

### <span data-ttu-id="d5079-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d5079-132">System.Boolean</span></span>

## <span data-ttu-id="d5079-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5079-133">NOTES</span></span>

## <span data-ttu-id="d5079-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5079-134">RELATED LINKS</span></span>

[<span data-ttu-id="d5079-135">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d5079-135">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="d5079-136">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d5079-136">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="d5079-137">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d5079-137">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


