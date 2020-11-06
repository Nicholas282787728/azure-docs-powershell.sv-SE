---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 11d832bc74aca4ac274ee17ff0b38de06b77e377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575393"
---
# <span data-ttu-id="df6f6-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="df6f6-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="df6f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="df6f6-103">Få information om Server delen.</span><span class="sxs-lookup"><span data-stu-id="df6f6-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df6f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df6f6-104">SYNTAX</span></span>

### <span data-ttu-id="df6f6-105">GetAllBackends (standard)</span><span class="sxs-lookup"><span data-stu-id="df6f6-105">GetAllBackends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df6f6-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="df6f6-106">GetByBackendId</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df6f6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df6f6-107">DESCRIPTION</span></span>
<span data-ttu-id="df6f6-108">Få information om Server delen.</span><span class="sxs-lookup"><span data-stu-id="df6f6-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="df6f6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df6f6-109">EXAMPLES</span></span>

### <span data-ttu-id="df6f6-110">Exempel 1: få alla bakände</span><span class="sxs-lookup"><span data-stu-id="df6f6-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="df6f6-111">Hämtar en lista över alla bakände som har kon figurer ATS i API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="df6f6-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="df6f6-112">Exempel 2: Hämta Server delen som anges av ID 123</span><span class="sxs-lookup"><span data-stu-id="df6f6-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="df6f6-113">Få information om den angivna Server delen som identifieras av identifieraren ' 123 '</span><span class="sxs-lookup"><span data-stu-id="df6f6-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="df6f6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df6f6-114">PARAMETERS</span></span>

### <span data-ttu-id="df6f6-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="df6f6-115">-BackendId</span></span>
<span data-ttu-id="df6f6-116">Identifierare för en server del.</span><span class="sxs-lookup"><span data-stu-id="df6f6-116">Identifier of a backend.</span></span>
<span data-ttu-id="df6f6-117">Om det här alternativet väljs kommer att försöka hitta server delen av identifieraren.</span><span class="sxs-lookup"><span data-stu-id="df6f6-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="df6f6-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="df6f6-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByBackendId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6f6-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="df6f6-119">-Context</span></span>
<span data-ttu-id="df6f6-120">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="df6f6-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="df6f6-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="df6f6-121">This parameter is required.</span></span>

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

### <span data-ttu-id="df6f6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df6f6-122">-DefaultProfile</span></span>
<span data-ttu-id="df6f6-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df6f6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df6f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df6f6-124">CommonParameters</span></span>
<span data-ttu-id="df6f6-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df6f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df6f6-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df6f6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df6f6-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df6f6-127">INPUTS</span></span>

### <span data-ttu-id="df6f6-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="df6f6-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="df6f6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="df6f6-129">System.String</span></span>

## <span data-ttu-id="df6f6-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df6f6-130">OUTPUTS</span></span>

### <span data-ttu-id="df6f6-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="df6f6-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="df6f6-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df6f6-132">NOTES</span></span>

## <span data-ttu-id="df6f6-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df6f6-133">RELATED LINKS</span></span>

[<span data-ttu-id="df6f6-134">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="df6f6-134">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="df6f6-135">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="df6f6-135">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="df6f6-136">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="df6f6-136">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="df6f6-137">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="df6f6-137">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="df6f6-138">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="df6f6-138">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
