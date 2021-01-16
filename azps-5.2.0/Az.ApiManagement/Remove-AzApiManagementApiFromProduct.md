---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: fd9e4cec821b08c9ac2bbd5cd2ac43e5e5b114ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409843"
---
# <span data-ttu-id="3054f-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="3054f-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="3054f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3054f-102">SYNOPSIS</span></span>
<span data-ttu-id="3054f-103">Tar bort ett API från en produkt.</span><span class="sxs-lookup"><span data-stu-id="3054f-103">Removes an API from a product.</span></span>

## <span data-ttu-id="3054f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3054f-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3054f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3054f-105">DESCRIPTION</span></span>
<span data-ttu-id="3054f-106">Cmdleten **Remove-AzApiManagementApiFromProduct** tar bort ett API för Azure API-hantering från en produkt.</span><span class="sxs-lookup"><span data-stu-id="3054f-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="3054f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3054f-107">EXAMPLES</span></span>

### <span data-ttu-id="3054f-108">Exempel 1: ta bort ett API från en produkt</span><span class="sxs-lookup"><span data-stu-id="3054f-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="3054f-109">Det här kommandot tar bort angivet API från en produkt.</span><span class="sxs-lookup"><span data-stu-id="3054f-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="3054f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3054f-110">PARAMETERS</span></span>

### <span data-ttu-id="3054f-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3054f-111">-ApiId</span></span>
<span data-ttu-id="3054f-112">Anger ID för det API som ska tas bort från produkten.</span><span class="sxs-lookup"><span data-stu-id="3054f-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="3054f-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3054f-113">-Context</span></span>
<span data-ttu-id="3054f-114">Anger en **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="3054f-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="3054f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3054f-115">-DefaultProfile</span></span>
<span data-ttu-id="3054f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3054f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3054f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3054f-117">-PassThru</span></span>
<span data-ttu-id="3054f-118">Anger att denna cmdlet returnerar ett värde för $True om det lyckas eller $False.</span><span class="sxs-lookup"><span data-stu-id="3054f-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="3054f-119">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="3054f-119">-ProductId</span></span>
<span data-ttu-id="3054f-120">Anger ID för den produkt som API: t ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="3054f-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="3054f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3054f-121">CommonParameters</span></span>
<span data-ttu-id="3054f-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3054f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3054f-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3054f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3054f-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3054f-124">INPUTS</span></span>

### <span data-ttu-id="3054f-125">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3054f-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3054f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3054f-126">System.String</span></span>

### <span data-ttu-id="3054f-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3054f-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3054f-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3054f-128">OUTPUTS</span></span>

### <span data-ttu-id="3054f-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3054f-129">System.Boolean</span></span>

## <span data-ttu-id="3054f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3054f-130">NOTES</span></span>

## <span data-ttu-id="3054f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3054f-131">RELATED LINKS</span></span>

[<span data-ttu-id="3054f-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="3054f-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


