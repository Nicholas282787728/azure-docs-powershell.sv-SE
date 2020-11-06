---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 505a26c48e53fe05e8724d61d5ddb66981e87ee9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573765"
---
# <span data-ttu-id="12b55-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="12b55-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="12b55-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12b55-102">SYNOPSIS</span></span>
<span data-ttu-id="12b55-103">Tar bort en befintlig API-produktnyckel.</span><span class="sxs-lookup"><span data-stu-id="12b55-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12b55-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12b55-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12b55-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12b55-105">DESCRIPTION</span></span>
<span data-ttu-id="12b55-106">Cmdleten **Remove-AzureRmApiManagementProduct** tar bort en befintlig API-hanterings produkt.</span><span class="sxs-lookup"><span data-stu-id="12b55-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="12b55-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12b55-107">EXAMPLES</span></span>

### <span data-ttu-id="12b55-108">Exempel 1: ta bort en befintlig produkt och alla abonnemang</span><span class="sxs-lookup"><span data-stu-id="12b55-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>Remove-AzureRmApiManagementProduct -Context $APImContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="12b55-109">Det här kommandot tar bort en befintlig produkt och alla prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="12b55-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="12b55-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12b55-110">PARAMETERS</span></span>

### <span data-ttu-id="12b55-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="12b55-111">-Context</span></span>
<span data-ttu-id="12b55-112">Anger en instans av **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="12b55-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="12b55-113">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="12b55-113">-DeleteSubscriptions</span></span>
<span data-ttu-id="12b55-114">Anger om du vill ta bort abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="12b55-114">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="12b55-115">Om du inte anger den här parametern och prenumerationen uppstår ett undantag.</span><span class="sxs-lookup"><span data-stu-id="12b55-115">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="12b55-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12b55-116">-PassThru</span></span>
<span data-ttu-id="12b55-117">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas, eller ett $False om det Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="12b55-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="12b55-118">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="12b55-118">-ProductId</span></span>
<span data-ttu-id="12b55-119">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="12b55-119">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="12b55-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="12b55-120">-Confirm</span></span>
<span data-ttu-id="12b55-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="12b55-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12b55-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12b55-122">-WhatIf</span></span>
<span data-ttu-id="12b55-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="12b55-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12b55-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="12b55-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12b55-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b55-125">-DefaultProfile</span></span>
<span data-ttu-id="12b55-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12b55-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12b55-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b55-127">CommonParameters</span></span>
<span data-ttu-id="12b55-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b55-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b55-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b55-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b55-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12b55-130">INPUTS</span></span>

## <span data-ttu-id="12b55-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12b55-131">OUTPUTS</span></span>

### <span data-ttu-id="12b55-132">bool</span><span class="sxs-lookup"><span data-stu-id="12b55-132">bool</span></span>

## <span data-ttu-id="12b55-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12b55-133">NOTES</span></span>

## <span data-ttu-id="12b55-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12b55-134">RELATED LINKS</span></span>

[<span data-ttu-id="12b55-135">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="12b55-135">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="12b55-136">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="12b55-136">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="12b55-137">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="12b55-137">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


