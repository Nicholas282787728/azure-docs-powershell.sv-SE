---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: 34631b2f1ac68e5f58c6269fa473dcf3d9103c7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917806"
---
# <span data-ttu-id="24cce-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="24cce-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="24cce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24cce-102">SYNOPSIS</span></span>
<span data-ttu-id="24cce-103">Tar bort ett API från en produkt.</span><span class="sxs-lookup"><span data-stu-id="24cce-103">Removes an API from a product.</span></span>

## <span data-ttu-id="24cce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24cce-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24cce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24cce-105">DESCRIPTION</span></span>
<span data-ttu-id="24cce-106">Cmdleten **Remove-AzApiManagementApiFromProduct** tar bort ett API för Azure API-hantering från en produkt.</span><span class="sxs-lookup"><span data-stu-id="24cce-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="24cce-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24cce-107">EXAMPLES</span></span>

### <span data-ttu-id="24cce-108">Exempel 1: ta bort ett API från en produkt</span><span class="sxs-lookup"><span data-stu-id="24cce-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="24cce-109">Denna commnd tar bort det angivna API: t från en produkt.</span><span class="sxs-lookup"><span data-stu-id="24cce-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="24cce-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24cce-110">PARAMETERS</span></span>

### <span data-ttu-id="24cce-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="24cce-111">-ApiId</span></span>
<span data-ttu-id="24cce-112">Anger ID för det API som ska tas bort från produkten.</span><span class="sxs-lookup"><span data-stu-id="24cce-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="24cce-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="24cce-113">-Context</span></span>
<span data-ttu-id="24cce-114">Anger en **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="24cce-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="24cce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24cce-115">-DefaultProfile</span></span>
<span data-ttu-id="24cce-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24cce-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24cce-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24cce-117">-PassThru</span></span>
<span data-ttu-id="24cce-118">Anger att denna cmdlet returnerar ett värde för $True om det lyckas eller $False.</span><span class="sxs-lookup"><span data-stu-id="24cce-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="24cce-119">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="24cce-119">-ProductId</span></span>
<span data-ttu-id="24cce-120">Anger ID för den produkt som API: t ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="24cce-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="24cce-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cce-121">CommonParameters</span></span>
<span data-ttu-id="24cce-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24cce-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cce-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24cce-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cce-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24cce-124">INPUTS</span></span>

### <span data-ttu-id="24cce-125">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="24cce-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="24cce-126">System. String</span><span class="sxs-lookup"><span data-stu-id="24cce-126">System.String</span></span>

### <span data-ttu-id="24cce-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="24cce-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="24cce-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24cce-128">OUTPUTS</span></span>

### <span data-ttu-id="24cce-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="24cce-129">System.Boolean</span></span>

## <span data-ttu-id="24cce-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24cce-130">NOTES</span></span>

## <span data-ttu-id="24cce-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24cce-131">RELATED LINKS</span></span>

[<span data-ttu-id="24cce-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="24cce-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


