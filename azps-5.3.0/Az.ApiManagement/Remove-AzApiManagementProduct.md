---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 33b00df9e0c9c5b5e0ef04d22b745942535effcb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423339"
---
# <span data-ttu-id="3d744-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3d744-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="3d744-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d744-102">SYNOPSIS</span></span>
<span data-ttu-id="3d744-103">Tar bort en befintlig API-produktnyckel.</span><span class="sxs-lookup"><span data-stu-id="3d744-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="3d744-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d744-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d744-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d744-105">DESCRIPTION</span></span>
<span data-ttu-id="3d744-106">Cmdleten **Remove-AzApiManagementProduct** tar bort en befintlig API-hanterings produkt.</span><span class="sxs-lookup"><span data-stu-id="3d744-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="3d744-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d744-107">EXAMPLES</span></span>

### <span data-ttu-id="3d744-108">Exempel 1: ta bort en befintlig produkt och alla abonnemang</span><span class="sxs-lookup"><span data-stu-id="3d744-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="3d744-109">Det här kommandot tar bort en befintlig produkt och alla prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="3d744-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="3d744-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d744-110">PARAMETERS</span></span>

### <span data-ttu-id="3d744-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3d744-111">-Context</span></span>
<span data-ttu-id="3d744-112">Anger en instans av **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="3d744-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3d744-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d744-113">-DefaultProfile</span></span>
<span data-ttu-id="3d744-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d744-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d744-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="3d744-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="3d744-116">Anger om du vill ta bort abonnemang för produkten.</span><span class="sxs-lookup"><span data-stu-id="3d744-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="3d744-117">Om du inte anger den här parametern och prenumerationen uppstår ett undantag.</span><span class="sxs-lookup"><span data-stu-id="3d744-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="3d744-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d744-118">-PassThru</span></span>
<span data-ttu-id="3d744-119">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas, eller ett $False om det Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="3d744-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="3d744-120">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="3d744-120">-ProductId</span></span>
<span data-ttu-id="3d744-121">Anger den befintliga produktens identifierare.</span><span class="sxs-lookup"><span data-stu-id="3d744-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="3d744-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d744-122">-Confirm</span></span>
<span data-ttu-id="3d744-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d744-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d744-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d744-124">-WhatIf</span></span>
<span data-ttu-id="3d744-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d744-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d744-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d744-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d744-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d744-127">CommonParameters</span></span>
<span data-ttu-id="3d744-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d744-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d744-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d744-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d744-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d744-130">INPUTS</span></span>

### <span data-ttu-id="3d744-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3d744-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3d744-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3d744-132">System.String</span></span>

### <span data-ttu-id="3d744-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3d744-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3d744-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d744-134">OUTPUTS</span></span>

### <span data-ttu-id="3d744-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d744-135">System.Boolean</span></span>

## <span data-ttu-id="3d744-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d744-136">NOTES</span></span>

## <span data-ttu-id="3d744-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d744-137">RELATED LINKS</span></span>

[<span data-ttu-id="3d744-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3d744-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="3d744-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3d744-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="3d744-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3d744-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


