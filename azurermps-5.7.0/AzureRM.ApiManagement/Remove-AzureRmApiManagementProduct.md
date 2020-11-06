---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 5c5bd7d0b7df385645bdb51d684616f2c0d7eaa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573576"
---
# <span data-ttu-id="a99c4-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a99c4-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="a99c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a99c4-102">SYNOPSIS</span></span>
<span data-ttu-id="a99c4-103">Tar bort en befintlig API-produktnyckel.</span><span class="sxs-lookup"><span data-stu-id="a99c4-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a99c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a99c4-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a99c4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a99c4-105">DESCRIPTION</span></span>
<span data-ttu-id="a99c4-106">Cmdleten **Remove-AzureRmApiManagementProduct** tar bort en befintlig API-hanterings produkt.</span><span class="sxs-lookup"><span data-stu-id="a99c4-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="a99c4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a99c4-107">EXAMPLES</span></span>

### <span data-ttu-id="a99c4-108">Exempel 1: ta bort en befintlig produkt och alla abonnemang</span><span class="sxs-lookup"><span data-stu-id="a99c4-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="a99c4-109">Det här kommandot tar bort en befintlig produkt och alla prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="a99c4-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="a99c4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a99c4-110">PARAMETERS</span></span>

### <span data-ttu-id="a99c4-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="a99c4-111">-Context</span></span>
<span data-ttu-id="a99c4-112">Anger en instans av **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="a99c4-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a99c4-113">-DefaultProfile</span></span>
<span data-ttu-id="a99c4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a99c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a99c4-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="a99c4-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="a99c4-116">Anger om du vill ta bort abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="a99c4-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="a99c4-117">Om du inte anger den här parametern och prenumerationen uppstår ett undantag.</span><span class="sxs-lookup"><span data-stu-id="a99c4-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99c4-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a99c4-118">-PassThru</span></span>
<span data-ttu-id="a99c4-119">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas, eller ett $False om det Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="a99c4-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99c4-120">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="a99c4-120">-ProductId</span></span>
<span data-ttu-id="a99c4-121">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="a99c4-121">Specifies the identifier of the existing product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a99c4-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a99c4-122">-Confirm</span></span>
<span data-ttu-id="a99c4-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a99c4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a99c4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a99c4-124">-WhatIf</span></span>
<span data-ttu-id="a99c4-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a99c4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a99c4-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a99c4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a99c4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99c4-127">CommonParameters</span></span>
<span data-ttu-id="a99c4-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a99c4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99c4-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a99c4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99c4-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a99c4-130">INPUTS</span></span>

### <span data-ttu-id="a99c4-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="a99c4-131">None</span></span>
<span data-ttu-id="a99c4-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a99c4-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a99c4-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a99c4-133">OUTPUTS</span></span>

### <span data-ttu-id="a99c4-134">bool</span><span class="sxs-lookup"><span data-stu-id="a99c4-134">bool</span></span>

## <span data-ttu-id="a99c4-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a99c4-135">NOTES</span></span>

## <span data-ttu-id="a99c4-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a99c4-136">RELATED LINKS</span></span>

[<span data-ttu-id="a99c4-137">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a99c4-137">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="a99c4-138">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a99c4-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="a99c4-139">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a99c4-139">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


