---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: b2c623d46dcc2d84e2c90ae5f3d94cfb54f7224a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578691"
---
# <span data-ttu-id="0ce65-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0ce65-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="0ce65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ce65-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce65-103">Hämtar en lista eller en angiven API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="0ce65-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ce65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ce65-104">SYNTAX</span></span>

### <span data-ttu-id="0ce65-105">Alla API-funktioner (standard)</span><span class="sxs-lookup"><span data-stu-id="0ce65-105">All API Operations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ce65-106">Sök efter ID</span><span class="sxs-lookup"><span data-stu-id="0ce65-106">Find by ID</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ce65-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ce65-107">DESCRIPTION</span></span>
<span data-ttu-id="0ce65-108">**Get-AzureRmApiManagementOperation** får en lista eller en angiven API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="0ce65-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="0ce65-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ce65-109">EXAMPLES</span></span>

### <span data-ttu-id="0ce65-110">Exempel 1: Hämta alla API-hanterings åtgärder</span><span class="sxs-lookup"><span data-stu-id="0ce65-110">Example 1: Get all API management operations</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId
```

<span data-ttu-id="0ce65-111">Det här kommandot får alla API-hanterings åtgärder.</span><span class="sxs-lookup"><span data-stu-id="0ce65-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="0ce65-112">Exempel 2: Hämta en API-hanterings åtgärd utifrån åtgärds-ID</span><span class="sxs-lookup"><span data-stu-id="0ce65-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="0ce65-113">Det här kommandot får en API-hantering med åtgärds-ID som heter Operation0003.</span><span class="sxs-lookup"><span data-stu-id="0ce65-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="0ce65-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ce65-114">PARAMETERS</span></span>

### <span data-ttu-id="0ce65-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0ce65-115">-ApiId</span></span>
<span data-ttu-id="0ce65-116">Anger API-funktionens identifierare.</span><span class="sxs-lookup"><span data-stu-id="0ce65-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="0ce65-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="0ce65-117">-Context</span></span>
<span data-ttu-id="0ce65-118">Anger instansen för **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="0ce65-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0ce65-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="0ce65-119">-OperationId</span></span>
<span data-ttu-id="0ce65-120">Anger Operations-ID.</span><span class="sxs-lookup"><span data-stu-id="0ce65-120">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ce65-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce65-121">-DefaultProfile</span></span>
<span data-ttu-id="0ce65-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ce65-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ce65-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce65-123">CommonParameters</span></span>
<span data-ttu-id="0ce65-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ce65-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce65-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ce65-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce65-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ce65-126">INPUTS</span></span>

## <span data-ttu-id="0ce65-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ce65-127">OUTPUTS</span></span>

### <span data-ttu-id="0ce65-128">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation></span><span class="sxs-lookup"><span data-stu-id="0ce65-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>

## <span data-ttu-id="0ce65-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ce65-129">NOTES</span></span>

## <span data-ttu-id="0ce65-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ce65-130">RELATED LINKS</span></span>

[<span data-ttu-id="0ce65-131">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0ce65-131">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="0ce65-132">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0ce65-132">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="0ce65-133">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0ce65-133">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


