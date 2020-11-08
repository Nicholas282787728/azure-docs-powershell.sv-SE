---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091677"
---
# <span data-ttu-id="c179d-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="c179d-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="c179d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c179d-102">SYNOPSIS</span></span>
<span data-ttu-id="c179d-103">Lägger till en produkt i en grupp.</span><span class="sxs-lookup"><span data-stu-id="c179d-103">Adds a product to a group.</span></span>

## <span data-ttu-id="c179d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c179d-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c179d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c179d-105">DESCRIPTION</span></span>
<span data-ttu-id="c179d-106">Cmdleten **Add-AzApiManagementProductToGroup** lägger till en produkt i en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="c179d-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="c179d-107">Med andra ord tilldelar denna cmdlet en grupp till en produkt.</span><span class="sxs-lookup"><span data-stu-id="c179d-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="c179d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c179d-108">EXAMPLES</span></span>

### <span data-ttu-id="c179d-109">Exempel 1: lägga till en produkt i en grupp</span><span class="sxs-lookup"><span data-stu-id="c179d-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="c179d-110">Det här kommandot lägger till en produkt i en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="c179d-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="c179d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c179d-111">PARAMETERS</span></span>

### <span data-ttu-id="c179d-112">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c179d-112">-Context</span></span>
<span data-ttu-id="c179d-113">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c179d-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="c179d-114">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c179d-114">This parameter is required.</span></span>

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

### <span data-ttu-id="c179d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c179d-115">-DefaultProfile</span></span>
<span data-ttu-id="c179d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c179d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c179d-117">-Kund-</span><span class="sxs-lookup"><span data-stu-id="c179d-117">-GroupId</span></span>
<span data-ttu-id="c179d-118">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="c179d-118">Specifies the group ID.</span></span>
<span data-ttu-id="c179d-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c179d-119">This parameter is required.</span></span>

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

### <span data-ttu-id="c179d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c179d-120">-PassThru</span></span>
<span data-ttu-id="c179d-121">passthru</span><span class="sxs-lookup"><span data-stu-id="c179d-121">passthru</span></span>

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

### <span data-ttu-id="c179d-122">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="c179d-122">-ProductId</span></span>
<span data-ttu-id="c179d-123">Anger produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="c179d-123">Specifies the product ID.</span></span>
<span data-ttu-id="c179d-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c179d-124">This parameter is required.</span></span>

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

### <span data-ttu-id="c179d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c179d-125">CommonParameters</span></span>
<span data-ttu-id="c179d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c179d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c179d-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c179d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c179d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c179d-128">INPUTS</span></span>

### <span data-ttu-id="c179d-129">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c179d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c179d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c179d-130">System.String</span></span>

### <span data-ttu-id="c179d-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c179d-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c179d-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c179d-132">OUTPUTS</span></span>

### <span data-ttu-id="c179d-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c179d-133">System.Boolean</span></span>

## <span data-ttu-id="c179d-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c179d-134">NOTES</span></span>

## <span data-ttu-id="c179d-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c179d-135">RELATED LINKS</span></span>

[<span data-ttu-id="c179d-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="c179d-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


