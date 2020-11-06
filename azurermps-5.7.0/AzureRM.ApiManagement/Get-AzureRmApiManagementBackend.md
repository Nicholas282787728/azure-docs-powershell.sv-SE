---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 0074ed7ec0d3aa88f813d138be71083195e6b10a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574454"
---
# <span data-ttu-id="53e23-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="53e23-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="53e23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53e23-102">SYNOPSIS</span></span>
<span data-ttu-id="53e23-103">Få information om Server delen.</span><span class="sxs-lookup"><span data-stu-id="53e23-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53e23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53e23-104">SYNTAX</span></span>

### <span data-ttu-id="53e23-105">GetAllBackends (standard)</span><span class="sxs-lookup"><span data-stu-id="53e23-105">GetAllBackends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53e23-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="53e23-106">GetByBackendId</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53e23-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53e23-107">DESCRIPTION</span></span>
<span data-ttu-id="53e23-108">Få information om Server delen.</span><span class="sxs-lookup"><span data-stu-id="53e23-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="53e23-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53e23-109">EXAMPLES</span></span>

### <span data-ttu-id="53e23-110">Exempel 1: få alla bakände</span><span class="sxs-lookup"><span data-stu-id="53e23-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="53e23-111">Hämtar en lista över alla bakände som har kon figurer ATS i API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="53e23-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="53e23-112">Exempel 2: Hämta Server delen som anges av ID 123</span><span class="sxs-lookup"><span data-stu-id="53e23-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="53e23-113">Få information om den angivna Server delen som identifieras av identifieraren ' 123 '</span><span class="sxs-lookup"><span data-stu-id="53e23-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="53e23-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53e23-114">PARAMETERS</span></span>

### <span data-ttu-id="53e23-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="53e23-115">-BackendId</span></span>
<span data-ttu-id="53e23-116">Identifierare för en server del.</span><span class="sxs-lookup"><span data-stu-id="53e23-116">Identifier of a backend.</span></span>
<span data-ttu-id="53e23-117">Om det här alternativet väljs kommer att försöka hitta server delen av identifieraren.</span><span class="sxs-lookup"><span data-stu-id="53e23-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="53e23-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="53e23-118">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByBackendId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53e23-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="53e23-119">-Context</span></span>
<span data-ttu-id="53e23-120">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="53e23-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="53e23-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="53e23-121">This parameter is required.</span></span>

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

### <span data-ttu-id="53e23-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53e23-122">-DefaultProfile</span></span>
<span data-ttu-id="53e23-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53e23-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="53e23-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53e23-124">CommonParameters</span></span>
<span data-ttu-id="53e23-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53e23-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53e23-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53e23-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53e23-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53e23-127">INPUTS</span></span>

### <span data-ttu-id="53e23-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="53e23-128">None</span></span>
<span data-ttu-id="53e23-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="53e23-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="53e23-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53e23-130">OUTPUTS</span></span>

### <span data-ttu-id="53e23-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="53e23-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>
<span data-ttu-id="53e23-132">Information om tjänst delen som kon figurer ATS i API Management Service.</span><span class="sxs-lookup"><span data-stu-id="53e23-132">The details of the Backend configured in API Management service.</span></span>

### <span data-ttu-id="53e23-133">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend></span><span class="sxs-lookup"><span data-stu-id="53e23-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend></span></span>
<span data-ttu-id="53e23-134">Listan över Server delen som har kon figurer ATS i API Management Service.</span><span class="sxs-lookup"><span data-stu-id="53e23-134">The list of Backend configured in API Management service.</span></span>

## <span data-ttu-id="53e23-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53e23-135">NOTES</span></span>

## <span data-ttu-id="53e23-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53e23-136">RELATED LINKS</span></span>

[<span data-ttu-id="53e23-137">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="53e23-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="53e23-138">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="53e23-138">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="53e23-139">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="53e23-139">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="53e23-140">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="53e23-140">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="53e23-141">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="53e23-141">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
