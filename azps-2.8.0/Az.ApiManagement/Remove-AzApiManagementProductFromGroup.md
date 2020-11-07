---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: 51f4caf679cf2440165e1808c152162d1f272d05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745696"
---
# <span data-ttu-id="68bb2-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="68bb2-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="68bb2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="68bb2-103">Tar bort en produkt från en grupp.</span><span class="sxs-lookup"><span data-stu-id="68bb2-103">Removes a product from a group.</span></span>

## <span data-ttu-id="68bb2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68bb2-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68bb2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68bb2-105">DESCRIPTION</span></span>
<span data-ttu-id="68bb2-106">Cmdleten **Remove-AzApiManagementProductFromGroup** tar bort en produkt från en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="68bb2-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="68bb2-107">Med andra ord tar denna cmdlet bort grupp tilldelningen från en produkt.</span><span class="sxs-lookup"><span data-stu-id="68bb2-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="68bb2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68bb2-108">EXAMPLES</span></span>

### <span data-ttu-id="68bb2-109">Exempel 1: ta bort en produkt från en grupp</span><span class="sxs-lookup"><span data-stu-id="68bb2-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="68bb2-110">Det här kommandot tar bort en produkt från en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="68bb2-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="68bb2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68bb2-111">PARAMETERS</span></span>

### <span data-ttu-id="68bb2-112">-Kontext</span><span class="sxs-lookup"><span data-stu-id="68bb2-112">-Context</span></span>
<span data-ttu-id="68bb2-113">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="68bb2-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="68bb2-114">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="68bb2-114">This parameter is required.</span></span>

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

### <span data-ttu-id="68bb2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68bb2-115">-DefaultProfile</span></span>
<span data-ttu-id="68bb2-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="68bb2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68bb2-117">-Kund-</span><span class="sxs-lookup"><span data-stu-id="68bb2-117">-GroupId</span></span>
<span data-ttu-id="68bb2-118">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="68bb2-118">Specifies the group ID.</span></span>
<span data-ttu-id="68bb2-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="68bb2-119">This parameter is required.</span></span>

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

### <span data-ttu-id="68bb2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68bb2-120">-PassThru</span></span>
<span data-ttu-id="68bb2-121">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller $False.</span><span class="sxs-lookup"><span data-stu-id="68bb2-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="68bb2-122">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="68bb2-122">-ProductId</span></span>
<span data-ttu-id="68bb2-123">Anger produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="68bb2-123">Specifies the product ID.</span></span>
<span data-ttu-id="68bb2-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="68bb2-124">This parameter is required.</span></span>

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

### <span data-ttu-id="68bb2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68bb2-125">CommonParameters</span></span>
<span data-ttu-id="68bb2-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68bb2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68bb2-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68bb2-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68bb2-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68bb2-128">INPUTS</span></span>

### <span data-ttu-id="68bb2-129">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="68bb2-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="68bb2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="68bb2-130">System.String</span></span>

### <span data-ttu-id="68bb2-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="68bb2-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="68bb2-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68bb2-132">OUTPUTS</span></span>

### <span data-ttu-id="68bb2-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68bb2-133">System.Boolean</span></span>

## <span data-ttu-id="68bb2-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68bb2-134">NOTES</span></span>

## <span data-ttu-id="68bb2-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68bb2-135">RELATED LINKS</span></span>

[<span data-ttu-id="68bb2-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="68bb2-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)

