---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 61a4ab9e7a827cffce861cc9ebaf7382e16e8fcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755560"
---
# <span data-ttu-id="6f985-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="6f985-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="6f985-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f985-102">SYNOPSIS</span></span>
<span data-ttu-id="6f985-103">Tar bort en befintlig API-produktnyckel.</span><span class="sxs-lookup"><span data-stu-id="6f985-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f985-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f985-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f985-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f985-105">DESCRIPTION</span></span>
<span data-ttu-id="6f985-106">Cmdleten **Remove-AzureRmApiManagementProduct** tar bort en befintlig API-hanterings produkt.</span><span class="sxs-lookup"><span data-stu-id="6f985-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="6f985-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f985-107">EXAMPLES</span></span>

### <span data-ttu-id="6f985-108">Exempel 1: ta bort en befintlig produkt och alla abonnemang</span><span class="sxs-lookup"><span data-stu-id="6f985-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="6f985-109">Det här kommandot tar bort en befintlig produkt och alla prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="6f985-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="6f985-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f985-110">PARAMETERS</span></span>

### <span data-ttu-id="6f985-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6f985-111">-Context</span></span>
<span data-ttu-id="6f985-112">Anger en instans av **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="6f985-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6f985-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f985-113">-DefaultProfile</span></span>
<span data-ttu-id="6f985-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f985-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f985-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="6f985-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="6f985-116">Anger om du vill ta bort abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="6f985-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="6f985-117">Om du inte anger den här parametern och prenumerationen uppstår ett undantag.</span><span class="sxs-lookup"><span data-stu-id="6f985-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="6f985-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f985-118">-PassThru</span></span>
<span data-ttu-id="6f985-119">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas, eller ett $False om det Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="6f985-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="6f985-120">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="6f985-120">-ProductId</span></span>
<span data-ttu-id="6f985-121">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="6f985-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="6f985-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6f985-122">-Confirm</span></span>
<span data-ttu-id="6f985-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6f985-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f985-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f985-124">-WhatIf</span></span>
<span data-ttu-id="6f985-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6f985-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f985-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6f985-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f985-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f985-127">CommonParameters</span></span>
<span data-ttu-id="6f985-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f985-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f985-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f985-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f985-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f985-130">INPUTS</span></span>

### <span data-ttu-id="6f985-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6f985-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6f985-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6f985-132">System.String</span></span>

### <span data-ttu-id="6f985-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6f985-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6f985-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f985-134">OUTPUTS</span></span>

### <span data-ttu-id="6f985-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f985-135">System.Boolean</span></span>

## <span data-ttu-id="6f985-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f985-136">NOTES</span></span>

## <span data-ttu-id="6f985-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f985-137">RELATED LINKS</span></span>

[<span data-ttu-id="6f985-138">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="6f985-138">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="6f985-139">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="6f985-139">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="6f985-140">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="6f985-140">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


