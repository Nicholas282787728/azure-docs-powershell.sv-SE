---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
ms.openlocfilehash: 2eba88e94cfed3c253a5b5febc20a7585ab096d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573577"
---
# <span data-ttu-id="ae944-101">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="ae944-101">Remove-AzureRmApiManagementProductFromGroup</span></span>

## <span data-ttu-id="ae944-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae944-102">SYNOPSIS</span></span>
<span data-ttu-id="ae944-103">Tar bort en produkt från en grupp.</span><span class="sxs-lookup"><span data-stu-id="ae944-103">Removes a product from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae944-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae944-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String>
 -ProductId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae944-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae944-105">DESCRIPTION</span></span>
<span data-ttu-id="ae944-106">Cmdleten **Remove-AzureRmApiManagementProductFromGroup** tar bort en produkt från en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="ae944-106">The **Remove-AzureRmApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="ae944-107">Med andra ord tar denna cmdlet bort grupp tilldelningen från en produkt.</span><span class="sxs-lookup"><span data-stu-id="ae944-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="ae944-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae944-108">EXAMPLES</span></span>

### <span data-ttu-id="ae944-109">Exempel 1: ta bort en produkt från en grupp</span><span class="sxs-lookup"><span data-stu-id="ae944-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="ae944-110">Det här kommandot tar bort en produkt från en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="ae944-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="ae944-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae944-111">PARAMETERS</span></span>

### <span data-ttu-id="ae944-112">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ae944-112">-Context</span></span>
<span data-ttu-id="ae944-113">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ae944-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="ae944-114">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ae944-114">This parameter is required.</span></span>

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

### <span data-ttu-id="ae944-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae944-115">-DefaultProfile</span></span>
<span data-ttu-id="ae944-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ae944-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="ae944-117">-Kund-</span><span class="sxs-lookup"><span data-stu-id="ae944-117">-GroupId</span></span>
<span data-ttu-id="ae944-118">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="ae944-118">Specifies the group ID.</span></span>
<span data-ttu-id="ae944-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ae944-119">This parameter is required.</span></span>

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

### <span data-ttu-id="ae944-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae944-120">-PassThru</span></span>
<span data-ttu-id="ae944-121">Anger att den här cmdleten returnerar ett värde för $True, om det lyckas eller $False.</span><span class="sxs-lookup"><span data-stu-id="ae944-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="ae944-122">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="ae944-122">-ProductId</span></span>
<span data-ttu-id="ae944-123">Anger produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="ae944-123">Specifies the product ID.</span></span>
<span data-ttu-id="ae944-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ae944-124">This parameter is required.</span></span>

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

### <span data-ttu-id="ae944-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae944-125">CommonParameters</span></span>
<span data-ttu-id="ae944-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae944-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae944-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae944-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae944-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae944-128">INPUTS</span></span>

### <span data-ttu-id="ae944-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="ae944-129">None</span></span>
<span data-ttu-id="ae944-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ae944-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ae944-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae944-131">OUTPUTS</span></span>

### <span data-ttu-id="ae944-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae944-132">System.Boolean</span></span>

## <span data-ttu-id="ae944-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae944-133">NOTES</span></span>

## <span data-ttu-id="ae944-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae944-134">RELATED LINKS</span></span>

[<span data-ttu-id="ae944-135">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="ae944-135">Add-AzureRmApiManagementProductToGroup</span></span>](./Add-AzureRmApiManagementProductToGroup.md)


