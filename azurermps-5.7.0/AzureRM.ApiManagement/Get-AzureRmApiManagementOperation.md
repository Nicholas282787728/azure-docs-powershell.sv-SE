---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: 1b1547485a4758764cf02eaca4fd7bc26d4ef990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582156"
---
# <span data-ttu-id="b0fca-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b0fca-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="b0fca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0fca-102">SYNOPSIS</span></span>
<span data-ttu-id="b0fca-103">Hämtar en lista eller en angiven API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="b0fca-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0fca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0fca-104">SYNTAX</span></span>

### <span data-ttu-id="b0fca-105">GetAllApiOperations (standard)</span><span class="sxs-lookup"><span data-stu-id="b0fca-105">GetAllApiOperations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0fca-106">GetById</span><span class="sxs-lookup"><span data-stu-id="b0fca-106">GetById</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0fca-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0fca-107">DESCRIPTION</span></span>
<span data-ttu-id="b0fca-108">**Get-AzureRmApiManagementOperation** får en lista eller en angiven API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="b0fca-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="b0fca-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0fca-109">EXAMPLES</span></span>

### <span data-ttu-id="b0fca-110">Exempel 1: Hämta alla API-hanterings åtgärder</span><span class="sxs-lookup"><span data-stu-id="b0fca-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="b0fca-111">Det här kommandot får alla API-hanterings åtgärder.</span><span class="sxs-lookup"><span data-stu-id="b0fca-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="b0fca-112">Exempel 2: Hämta en API-hanterings åtgärd utifrån åtgärds-ID</span><span class="sxs-lookup"><span data-stu-id="b0fca-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="b0fca-113">Det här kommandot får en API-hantering med åtgärds-ID som heter Operation0003.</span><span class="sxs-lookup"><span data-stu-id="b0fca-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="b0fca-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0fca-114">PARAMETERS</span></span>

### <span data-ttu-id="b0fca-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b0fca-115">-ApiId</span></span>
<span data-ttu-id="b0fca-116">Anger API-funktionens identifierare.</span><span class="sxs-lookup"><span data-stu-id="b0fca-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="b0fca-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b0fca-117">-Context</span></span>
<span data-ttu-id="b0fca-118">Anger instansen för **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="b0fca-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b0fca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0fca-119">-DefaultProfile</span></span>
<span data-ttu-id="b0fca-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0fca-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="b0fca-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="b0fca-121">-OperationId</span></span>
<span data-ttu-id="b0fca-122">Anger Operations-ID.</span><span class="sxs-lookup"><span data-stu-id="b0fca-122">Specifies the operation identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0fca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0fca-123">CommonParameters</span></span>
<span data-ttu-id="b0fca-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0fca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0fca-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0fca-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0fca-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0fca-126">INPUTS</span></span>

### <span data-ttu-id="b0fca-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="b0fca-127">None</span></span>
<span data-ttu-id="b0fca-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b0fca-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b0fca-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0fca-129">OUTPUTS</span></span>

### <span data-ttu-id="b0fca-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b0fca-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>
<span data-ttu-id="b0fca-131">Information om API-åtgärden i API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b0fca-131">The details of the API Operation in Api Management service.</span></span>

### <span data-ttu-id="b0fca-132">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation></span><span class="sxs-lookup"><span data-stu-id="b0fca-132">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>
<span data-ttu-id="b0fca-133">Listan över API-åtgärd i API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="b0fca-133">The list of API Operation in Api Management service.</span></span>

## <span data-ttu-id="b0fca-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0fca-134">NOTES</span></span>

## <span data-ttu-id="b0fca-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0fca-135">RELATED LINKS</span></span>

[<span data-ttu-id="b0fca-136">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b0fca-136">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="b0fca-137">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b0fca-137">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="b0fca-138">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b0fca-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


