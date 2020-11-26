---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: 01767d80f0925647b2161dd26f504465d7f1d8e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321972"
---
# <span data-ttu-id="19a77-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="19a77-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="19a77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19a77-102">SYNOPSIS</span></span>
<span data-ttu-id="19a77-103">Lägger till ett API till en produkt.</span><span class="sxs-lookup"><span data-stu-id="19a77-103">Adds an API to a product.</span></span>

## <span data-ttu-id="19a77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19a77-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19a77-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19a77-105">DESCRIPTION</span></span>
<span data-ttu-id="19a77-106">Cmdleten **Add-AzApiManagementApiToProduct** lägger till ett API för Azure API-hantering till en produkt.</span><span class="sxs-lookup"><span data-stu-id="19a77-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="19a77-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19a77-107">EXAMPLES</span></span>

### <span data-ttu-id="19a77-108">Exempel 1: lägga till ett API till en produkt</span><span class="sxs-lookup"><span data-stu-id="19a77-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="19a77-109">Det här kommandot lägger till angivet API till den angivna produkten.</span><span class="sxs-lookup"><span data-stu-id="19a77-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="19a77-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19a77-110">PARAMETERS</span></span>

### <span data-ttu-id="19a77-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="19a77-111">-ApiId</span></span>
<span data-ttu-id="19a77-112">Anger ID för ett API att lägga till i en produkt.</span><span class="sxs-lookup"><span data-stu-id="19a77-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="19a77-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="19a77-113">-Context</span></span>
<span data-ttu-id="19a77-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="19a77-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="19a77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19a77-115">-DefaultProfile</span></span>
<span data-ttu-id="19a77-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="19a77-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19a77-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19a77-117">-PassThru</span></span>
<span data-ttu-id="19a77-118">passthru</span><span class="sxs-lookup"><span data-stu-id="19a77-118">passthru</span></span>

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

### <span data-ttu-id="19a77-119">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="19a77-119">-ProductId</span></span>
<span data-ttu-id="19a77-120">Anger ID: t för den produkt som du vill lägga till API: t.</span><span class="sxs-lookup"><span data-stu-id="19a77-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="19a77-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19a77-121">CommonParameters</span></span>
<span data-ttu-id="19a77-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19a77-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19a77-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19a77-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19a77-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19a77-124">INPUTS</span></span>

### <span data-ttu-id="19a77-125">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="19a77-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="19a77-126">System. String</span><span class="sxs-lookup"><span data-stu-id="19a77-126">System.String</span></span>

### <span data-ttu-id="19a77-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="19a77-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="19a77-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19a77-128">OUTPUTS</span></span>

### <span data-ttu-id="19a77-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19a77-129">System.Boolean</span></span>

## <span data-ttu-id="19a77-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19a77-130">NOTES</span></span>

## <span data-ttu-id="19a77-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19a77-131">RELATED LINKS</span></span>

[<span data-ttu-id="19a77-132">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="19a77-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)

