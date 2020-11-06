---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: b4e1a029eca4e7eda48f44d85292639767eaf845
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581567"
---
# <span data-ttu-id="5fea2-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="5fea2-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="5fea2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fea2-102">SYNOPSIS</span></span>
<span data-ttu-id="5fea2-103">Lägger till en produkt i en grupp.</span><span class="sxs-lookup"><span data-stu-id="5fea2-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fea2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fea2-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fea2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fea2-105">DESCRIPTION</span></span>
<span data-ttu-id="5fea2-106">Cmdleten **Add-AzureRmApiManagementProductToGroup** lägger till en produkt i en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="5fea2-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="5fea2-107">Med andra ord tilldelar denna cmdlet en grupp till en produkt.</span><span class="sxs-lookup"><span data-stu-id="5fea2-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="5fea2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fea2-108">EXAMPLES</span></span>

### <span data-ttu-id="5fea2-109">Exempel 1: lägga till en produkt i en grupp</span><span class="sxs-lookup"><span data-stu-id="5fea2-109">Example 1: Add a product to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="5fea2-110">Det här kommandot lägger till en produkt i en befintlig grupp.</span><span class="sxs-lookup"><span data-stu-id="5fea2-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="5fea2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fea2-111">PARAMETERS</span></span>

### <span data-ttu-id="5fea2-112">-Kontext</span><span class="sxs-lookup"><span data-stu-id="5fea2-112">-Context</span></span>
<span data-ttu-id="5fea2-113">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="5fea2-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="5fea2-114">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="5fea2-114">This parameter is required.</span></span>

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

### <span data-ttu-id="5fea2-115">-Kund-</span><span class="sxs-lookup"><span data-stu-id="5fea2-115">-GroupId</span></span>
<span data-ttu-id="5fea2-116">Anger grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="5fea2-116">Specifies the group ID.</span></span>
<span data-ttu-id="5fea2-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="5fea2-117">This parameter is required.</span></span>

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

### <span data-ttu-id="5fea2-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5fea2-118">-PassThru</span></span>
<span data-ttu-id="5fea2-119">passthru</span><span class="sxs-lookup"><span data-stu-id="5fea2-119">passthru</span></span>

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

### <span data-ttu-id="5fea2-120">-Produktnr</span><span class="sxs-lookup"><span data-stu-id="5fea2-120">-ProductId</span></span>
<span data-ttu-id="5fea2-121">Anger produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="5fea2-121">Specifies the product ID.</span></span>
<span data-ttu-id="5fea2-122">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="5fea2-122">This parameter is required.</span></span>

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

### <span data-ttu-id="5fea2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fea2-123">-DefaultProfile</span></span>
<span data-ttu-id="5fea2-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5fea2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fea2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fea2-125">CommonParameters</span></span>
<span data-ttu-id="5fea2-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fea2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fea2-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fea2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fea2-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fea2-128">INPUTS</span></span>

## <span data-ttu-id="5fea2-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fea2-129">OUTPUTS</span></span>

### <span data-ttu-id="5fea2-130">Returtyp</span><span class="sxs-lookup"><span data-stu-id="5fea2-130">Boolean</span></span>

## <span data-ttu-id="5fea2-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fea2-131">NOTES</span></span>

## <span data-ttu-id="5fea2-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fea2-132">RELATED LINKS</span></span>

[<span data-ttu-id="5fea2-133">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="5fea2-133">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


