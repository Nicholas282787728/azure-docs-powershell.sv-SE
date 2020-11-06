---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: fd232a0f118db5730c41ef1588eaf07d80df69f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573755"
---
# <span data-ttu-id="276b2-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="276b2-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="276b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="276b2-102">SYNOPSIS</span></span>
<span data-ttu-id="276b2-103">Tar bort ett befintligt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="276b2-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="276b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="276b2-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="276b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="276b2-105">DESCRIPTION</span></span>
<span data-ttu-id="276b2-106">Cmdleten **Remove-AzureRmApiManagementSubscription** tar bort en befintlig prenumeration.</span><span class="sxs-lookup"><span data-stu-id="276b2-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="276b2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="276b2-107">EXAMPLES</span></span>

### <span data-ttu-id="276b2-108">Exempel 1: ta bort ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="276b2-108">Example 1: Delete a subscription</span></span>
```
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="276b2-109">Det här kommandot tar bort ett befintligt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="276b2-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="276b2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="276b2-110">PARAMETERS</span></span>

### <span data-ttu-id="276b2-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="276b2-111">-Context</span></span>
<span data-ttu-id="276b2-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="276b2-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="276b2-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="276b2-113">-PassThru</span></span>
<span data-ttu-id="276b2-114">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller ett $false värde.</span><span class="sxs-lookup"><span data-stu-id="276b2-114">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="276b2-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="276b2-115">-SubscriptionId</span></span>
<span data-ttu-id="276b2-116">Anger abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="276b2-116">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="276b2-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="276b2-117">-Confirm</span></span>
<span data-ttu-id="276b2-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="276b2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="276b2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="276b2-119">-WhatIf</span></span>
<span data-ttu-id="276b2-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="276b2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="276b2-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="276b2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="276b2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="276b2-122">-DefaultProfile</span></span>
<span data-ttu-id="276b2-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="276b2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="276b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="276b2-124">CommonParameters</span></span>
<span data-ttu-id="276b2-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="276b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="276b2-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="276b2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="276b2-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="276b2-127">INPUTS</span></span>

## <span data-ttu-id="276b2-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="276b2-128">OUTPUTS</span></span>

### <span data-ttu-id="276b2-129">Returtyp</span><span class="sxs-lookup"><span data-stu-id="276b2-129">Boolean</span></span>

## <span data-ttu-id="276b2-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="276b2-130">NOTES</span></span>

## <span data-ttu-id="276b2-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="276b2-131">RELATED LINKS</span></span>

[<span data-ttu-id="276b2-132">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="276b2-132">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="276b2-133">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="276b2-133">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="276b2-134">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="276b2-134">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


