---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: f7c1db6b4ce7c9df63506cdba8b1a206c22ee03e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758238"
---
# <span data-ttu-id="3d84c-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="3d84c-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="3d84c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d84c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d84c-103">Lägger till en produkt i en grupp.</span><span class="sxs-lookup"><span data-stu-id="3d84c-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d84c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d84c-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d84c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d84c-105">DESCRIPTION</span></span>
<span data-ttu-id="3d84c-106">Cmdleten **Add-AzureRmApiManagementProductToGroup** lägger till en produkt i en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="3d84c-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="3d84c-107">Med andra ord tilldelar denna cmdlet en grupp till en produkt.</span><span class="sxs-lookup"><span data-stu-id="3d84c-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="3d84c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d84c-108">EXAMPLES</span></span>

### <span data-ttu-id="3d84c-109">Exempel 1: lägga till en produkt i en grupp</span><span class="sxs-lookup"><span data-stu-id="3d84c-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="3d84c-110">Det här kommandot lägger till en produkt i en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="3d84c-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="3d84c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d84c-111">PARAMETERS</span></span>

### <span data-ttu-id="3d84c-112">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3d84c-112">-Context</span></span>
<span data-ttu-id="3d84c-113">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3d84c-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="3d84c-114">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="3d84c-114">This parameter is required.</span></span>

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

### <span data-ttu-id="3d84c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d84c-115">-DefaultProfile</span></span>
<span data-ttu-id="3d84c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d84c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3d84c-117">-Kund-</span><span class="sxs-lookup"><span data-stu-id="3d84c-117">-GroupId</span></span>
<span data-ttu-id="3d84c-118">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="3d84c-118">Specifies the group ID.</span></span>
<span data-ttu-id="3d84c-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="3d84c-119">This parameter is required.</span></span>

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

### <span data-ttu-id="3d84c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d84c-120">-PassThru</span></span>
<span data-ttu-id="3d84c-121">passthru</span><span class="sxs-lookup"><span data-stu-id="3d84c-121">passthru</span></span>

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

### <span data-ttu-id="3d84c-122">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="3d84c-122">-ProductId</span></span>
<span data-ttu-id="3d84c-123">Anger produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="3d84c-123">Specifies the product ID.</span></span>
<span data-ttu-id="3d84c-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="3d84c-124">This parameter is required.</span></span>

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

### <span data-ttu-id="3d84c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d84c-125">CommonParameters</span></span>
<span data-ttu-id="3d84c-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d84c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d84c-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d84c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d84c-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d84c-128">INPUTS</span></span>

### <span data-ttu-id="3d84c-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="3d84c-129">None</span></span>
<span data-ttu-id="3d84c-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3d84c-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d84c-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d84c-131">OUTPUTS</span></span>

### <span data-ttu-id="3d84c-132">Returtyp</span><span class="sxs-lookup"><span data-stu-id="3d84c-132">Boolean</span></span>

## <span data-ttu-id="3d84c-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d84c-133">NOTES</span></span>

## <span data-ttu-id="3d84c-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d84c-134">RELATED LINKS</span></span>

[<span data-ttu-id="3d84c-135">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="3d84c-135">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


