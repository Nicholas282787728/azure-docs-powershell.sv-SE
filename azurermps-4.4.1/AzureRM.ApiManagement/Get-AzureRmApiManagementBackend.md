---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 4f54b361482bad24826d7120e53f96ce8d3b9eef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579868"
---
# <span data-ttu-id="dd2fd-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd2fd-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="dd2fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd2fd-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2fd-103">Få information om Server delen.</span><span class="sxs-lookup"><span data-stu-id="dd2fd-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd2fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd2fd-104">SYNTAX</span></span>

### <span data-ttu-id="dd2fd-105">Få alla bakände (standard)</span><span class="sxs-lookup"><span data-stu-id="dd2fd-105">Get all backends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd2fd-106">Hämta via server dels-ID</span><span class="sxs-lookup"><span data-stu-id="dd2fd-106">Get by backend ID</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd2fd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd2fd-107">DESCRIPTION</span></span>
<span data-ttu-id="dd2fd-108">Få information om Server delen.</span><span class="sxs-lookup"><span data-stu-id="dd2fd-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="dd2fd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd2fd-109">EXAMPLES</span></span>

### <span data-ttu-id="dd2fd-110">--------------------------Exempel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dd2fd-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="dd2fd-111">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="dd2fd-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="dd2fd-112">Hämtar en lista över alla bakände som har kon figurer ATS i API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="dd2fd-112">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="dd2fd-113">--------------------------Exempel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="dd2fd-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="dd2fd-114">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="dd2fd-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="dd2fd-115">Få information om den angivna Server delen som identifieras av identifieraren ' 123 '</span><span class="sxs-lookup"><span data-stu-id="dd2fd-115">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="dd2fd-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd2fd-116">PARAMETERS</span></span>

### <span data-ttu-id="dd2fd-117">-BackendId</span><span class="sxs-lookup"><span data-stu-id="dd2fd-117">-BackendId</span></span>
<span data-ttu-id="dd2fd-118">Identifierare för en server del.</span><span class="sxs-lookup"><span data-stu-id="dd2fd-118">Identifier of a backend.</span></span>
<span data-ttu-id="dd2fd-119">Om det här alternativet väljs kommer att försöka hitta server delen av identifieraren.</span><span class="sxs-lookup"><span data-stu-id="dd2fd-119">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="dd2fd-120">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="dd2fd-120">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by backend ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd2fd-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="dd2fd-121">-Context</span></span>
<span data-ttu-id="dd2fd-122">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="dd2fd-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dd2fd-123">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="dd2fd-123">This parameter is required.</span></span>

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

### <span data-ttu-id="dd2fd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd2fd-124">-DefaultProfile</span></span>
<span data-ttu-id="dd2fd-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd2fd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd2fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2fd-126">CommonParameters</span></span>
<span data-ttu-id="dd2fd-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd2fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd2fd-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd2fd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2fd-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd2fd-129">INPUTS</span></span>

## <span data-ttu-id="dd2fd-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd2fd-130">OUTPUTS</span></span>

### <span data-ttu-id="dd2fd-131">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend></span><span class="sxs-lookup"><span data-stu-id="dd2fd-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend></span></span>

### <span data-ttu-id="dd2fd-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd2fd-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger.PsApiManagementBackend</span></span>

## <span data-ttu-id="dd2fd-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd2fd-133">NOTES</span></span>

## <span data-ttu-id="dd2fd-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd2fd-134">RELATED LINKS</span></span>

[<span data-ttu-id="dd2fd-135">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd2fd-135">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="dd2fd-136">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="dd2fd-136">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="dd2fd-137">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="dd2fd-137">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="dd2fd-138">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd2fd-138">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="dd2fd-139">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd2fd-139">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
