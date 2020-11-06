---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: 58f80b6ff1742bfc6360844648d6ad18d12d8389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578648"
---
# <span data-ttu-id="0ee64-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="0ee64-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="0ee64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ee64-102">SYNOPSIS</span></span>
<span data-ttu-id="0ee64-103">Skapar ett nytt kontrakt för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="0ee64-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ee64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ee64-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ee64-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ee64-105">DESCRIPTION</span></span>
<span data-ttu-id="0ee64-106">Skapar ett nytt kontrakt för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="0ee64-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="0ee64-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ee64-107">EXAMPLES</span></span>

### <span data-ttu-id="0ee64-108">Skapa en server dels referenser In-Memory objekt</span><span class="sxs-lookup"><span data-stu-id="0ee64-108">Create a Backend Credentials In-Memory Object</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}
```

<span data-ttu-id="0ee64-109">Skapar ett kontrakt för inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="0ee64-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="0ee64-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ee64-110">PARAMETERS</span></span>

### <span data-ttu-id="0ee64-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="0ee64-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="0ee64-112">Huvud tillstånd som används för Server delen.</span><span class="sxs-lookup"><span data-stu-id="0ee64-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="0ee64-113">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0ee64-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="0ee64-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="0ee64-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="0ee64-115">Godkännande schema som används för Server delen.</span><span class="sxs-lookup"><span data-stu-id="0ee64-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="0ee64-116">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0ee64-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="0ee64-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="0ee64-117">-CertificateThumbprint</span></span>
<span data-ttu-id="0ee64-118">Thumbprints för klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="0ee64-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="0ee64-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0ee64-119">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ee64-120">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="0ee64-120">-Header</span></span>
<span data-ttu-id="0ee64-121">Rubrik parameter värden som accepteras av Server delen.</span><span class="sxs-lookup"><span data-stu-id="0ee64-121">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="0ee64-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0ee64-122">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ee64-123">-Fråga</span><span class="sxs-lookup"><span data-stu-id="0ee64-123">-Query</span></span>
<span data-ttu-id="0ee64-124">Parameter värden för frågor som accepteras av Server delen.</span><span class="sxs-lookup"><span data-stu-id="0ee64-124">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="0ee64-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0ee64-125">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ee64-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ee64-126">-DefaultProfile</span></span>
<span data-ttu-id="0ee64-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ee64-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ee64-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ee64-128">CommonParameters</span></span>
<span data-ttu-id="0ee64-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ee64-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ee64-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ee64-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ee64-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ee64-131">INPUTS</span></span>

## <span data-ttu-id="0ee64-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ee64-132">OUTPUTS</span></span>

### <span data-ttu-id="0ee64-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="0ee64-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="0ee64-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ee64-134">NOTES</span></span>

## <span data-ttu-id="0ee64-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ee64-135">RELATED LINKS</span></span>

[<span data-ttu-id="0ee64-136">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0ee64-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="0ee64-137">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0ee64-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="0ee64-138">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="0ee64-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="0ee64-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0ee64-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="0ee64-140">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0ee64-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
