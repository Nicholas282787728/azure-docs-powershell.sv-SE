---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d3699347d21f17452d521afb3bc5524f8e68e40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578640"
---
# <span data-ttu-id="69f5d-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="69f5d-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="69f5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="69f5d-103">Skapar ett nytt Server dels proxyobjekt.</span><span class="sxs-lookup"><span data-stu-id="69f5d-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69f5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69f5d-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-UserName <String>] [-Password <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69f5d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69f5d-105">DESCRIPTION</span></span>
<span data-ttu-id="69f5d-106">Skapar ett nytt backend-proxyobjekt som kan vara piped när du skapar en ny backend-enhet.</span><span class="sxs-lookup"><span data-stu-id="69f5d-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="69f5d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69f5d-107">EXAMPLES</span></span>

### <span data-ttu-id="69f5d-108">Skapa ett In-Memory objekt i en del av Server delen</span><span class="sxs-lookup"><span data-stu-id="69f5d-108">Create a Backend Proxy In-Memory Object</span></span>
```
$proxy= New-AzureRmApiManagementBackendProxy -Url "https://abbc.def.g" -UserName "apim" -Password "password"
```

<span data-ttu-id="69f5d-109">Skapar ett objekt i en del av Server delen</span><span class="sxs-lookup"><span data-stu-id="69f5d-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="69f5d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69f5d-110">PARAMETERS</span></span>

### <span data-ttu-id="69f5d-111">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="69f5d-111">-Password</span></span>
<span data-ttu-id="69f5d-112">Lösen ord som används för att ansluta till backend-proxyservern.</span><span class="sxs-lookup"><span data-stu-id="69f5d-112">Proxy Password used to connect to Backend Proxy.</span></span>
<span data-ttu-id="69f5d-113">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="69f5d-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69f5d-114">-URL</span><span class="sxs-lookup"><span data-stu-id="69f5d-114">-Url</span></span>
<span data-ttu-id="69f5d-115">URL-adressen till den proxyserver som ska användas vid vidarekoppling av samtal till Server delen.</span><span class="sxs-lookup"><span data-stu-id="69f5d-115">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="69f5d-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="69f5d-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69f5d-117">-UserName</span><span class="sxs-lookup"><span data-stu-id="69f5d-117">-UserName</span></span>
<span data-ttu-id="69f5d-118">Proxy-användarnamn som används för att ansluta till backend-proxyservern.</span><span class="sxs-lookup"><span data-stu-id="69f5d-118">Proxy UserName used to connect to Backend Proxy.</span></span>
<span data-ttu-id="69f5d-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="69f5d-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69f5d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f5d-120">-DefaultProfile</span></span>
<span data-ttu-id="69f5d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="69f5d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69f5d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f5d-122">CommonParameters</span></span>
<span data-ttu-id="69f5d-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69f5d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f5d-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69f5d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f5d-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69f5d-125">INPUTS</span></span>

## <span data-ttu-id="69f5d-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69f5d-126">OUTPUTS</span></span>

### <span data-ttu-id="69f5d-127">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="69f5d-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="69f5d-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69f5d-128">NOTES</span></span>

## <span data-ttu-id="69f5d-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69f5d-129">RELATED LINKS</span></span>

[<span data-ttu-id="69f5d-130">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="69f5d-130">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="69f5d-131">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="69f5d-131">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="69f5d-132">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="69f5d-132">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="69f5d-133">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="69f5d-133">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="69f5d-134">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="69f5d-134">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
