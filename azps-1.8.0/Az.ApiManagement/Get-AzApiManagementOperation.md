---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 8fdfa75e78d48fb582af869a240476bfff31f25d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743405"
---
# <span data-ttu-id="ef68f-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ef68f-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="ef68f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef68f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef68f-103">Hämtar en lista eller en angiven API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="ef68f-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="ef68f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef68f-104">SYNTAX</span></span>

### <span data-ttu-id="ef68f-105">GetAllApiOperations (standard)</span><span class="sxs-lookup"><span data-stu-id="ef68f-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef68f-106">GetById</span><span class="sxs-lookup"><span data-stu-id="ef68f-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef68f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef68f-107">DESCRIPTION</span></span>
<span data-ttu-id="ef68f-108">**Get-AzApiManagementOperation** får en lista eller en angiven API-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="ef68f-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="ef68f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef68f-109">EXAMPLES</span></span>

### <span data-ttu-id="ef68f-110">Exempel 1: Hämta alla API-hanterings åtgärder</span><span class="sxs-lookup"><span data-stu-id="ef68f-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="ef68f-111">Det här kommandot får alla API-hanterings åtgärder.</span><span class="sxs-lookup"><span data-stu-id="ef68f-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="ef68f-112">Exempel 2: Hämta en API-hanterings åtgärd utifrån åtgärds-ID</span><span class="sxs-lookup"><span data-stu-id="ef68f-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="ef68f-113">Det här kommandot får en API-hantering med åtgärds-ID som heter Operation0003.</span><span class="sxs-lookup"><span data-stu-id="ef68f-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="ef68f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef68f-114">PARAMETERS</span></span>

### <span data-ttu-id="ef68f-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ef68f-115">-ApiId</span></span>
<span data-ttu-id="ef68f-116">Anger API-funktionens identifierare.</span><span class="sxs-lookup"><span data-stu-id="ef68f-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="ef68f-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="ef68f-117">-ApiRevision</span></span>
<span data-ttu-id="ef68f-118">Identifierare för API-revision.</span><span class="sxs-lookup"><span data-stu-id="ef68f-118">Identifier of API Revision.</span></span> <span data-ttu-id="ef68f-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ef68f-119">This parameter is optional.</span></span> <span data-ttu-id="ef68f-120">Om det inte anges hämtas åtgärden från den för tillfället aktiva API-ändringen.</span><span class="sxs-lookup"><span data-stu-id="ef68f-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef68f-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ef68f-121">-Context</span></span>
<span data-ttu-id="ef68f-122">Anger instansen för **PsApiManagementContext** -objektet.</span><span class="sxs-lookup"><span data-stu-id="ef68f-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ef68f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef68f-123">-DefaultProfile</span></span>
<span data-ttu-id="ef68f-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef68f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef68f-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ef68f-125">-OperationId</span></span>
<span data-ttu-id="ef68f-126">Anger Operations-ID.</span><span class="sxs-lookup"><span data-stu-id="ef68f-126">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef68f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef68f-127">CommonParameters</span></span>
<span data-ttu-id="ef68f-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef68f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef68f-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef68f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef68f-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef68f-130">INPUTS</span></span>

### <span data-ttu-id="ef68f-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ef68f-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ef68f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ef68f-132">System.String</span></span>

## <span data-ttu-id="ef68f-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef68f-133">OUTPUTS</span></span>

### <span data-ttu-id="ef68f-134">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ef68f-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="ef68f-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef68f-135">NOTES</span></span>

## <span data-ttu-id="ef68f-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef68f-136">RELATED LINKS</span></span>

[<span data-ttu-id="ef68f-137">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ef68f-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="ef68f-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ef68f-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="ef68f-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ef68f-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)

