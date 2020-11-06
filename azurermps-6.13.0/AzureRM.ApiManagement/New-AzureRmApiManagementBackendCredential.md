---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendCredential.md
ms.openlocfilehash: d34a7666e10fe678d49194887d9b58e7c1ba0aa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575380"
---
# <span data-ttu-id="1f83a-101">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1f83a-101">New-AzureRmApiManagementBackendCredential</span></span>

## <span data-ttu-id="1f83a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f83a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f83a-103">Skapar ett nytt kontrakt för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="1f83a-103">Creates a new Backend Credential contract.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f83a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f83a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f83a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f83a-105">DESCRIPTION</span></span>
<span data-ttu-id="1f83a-106">Skapar ett nytt kontrakt för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="1f83a-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="1f83a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f83a-107">EXAMPLES</span></span>

### <span data-ttu-id="1f83a-108">Skapa en server dels referenser In-Memory objekt</span><span class="sxs-lookup"><span data-stu-id="1f83a-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="1f83a-109">Skapar ett kontrakt för inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="1f83a-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="1f83a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f83a-110">PARAMETERS</span></span>

### <span data-ttu-id="1f83a-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="1f83a-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="1f83a-112">Huvud tillstånd som används för Server delen.</span><span class="sxs-lookup"><span data-stu-id="1f83a-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="1f83a-113">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="1f83a-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="1f83a-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="1f83a-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="1f83a-115">Godkännande schema som används för Server delen.</span><span class="sxs-lookup"><span data-stu-id="1f83a-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="1f83a-116">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="1f83a-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="1f83a-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="1f83a-117">-CertificateThumbprint</span></span>
<span data-ttu-id="1f83a-118">Thumbprints för klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="1f83a-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="1f83a-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="1f83a-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="1f83a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f83a-120">-DefaultProfile</span></span>
<span data-ttu-id="1f83a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f83a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f83a-122">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="1f83a-122">-Header</span></span>
<span data-ttu-id="1f83a-123">Rubrik parameter värden som accepteras av Server delen.</span><span class="sxs-lookup"><span data-stu-id="1f83a-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="1f83a-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="1f83a-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="1f83a-125">-Fråga</span><span class="sxs-lookup"><span data-stu-id="1f83a-125">-Query</span></span>
<span data-ttu-id="1f83a-126">Parameter värden för frågor som accepteras av Server delen.</span><span class="sxs-lookup"><span data-stu-id="1f83a-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="1f83a-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="1f83a-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="1f83a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f83a-128">CommonParameters</span></span>
<span data-ttu-id="1f83a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f83a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f83a-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f83a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f83a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f83a-131">INPUTS</span></span>

### <span data-ttu-id="1f83a-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="1f83a-132">None</span></span>

## <span data-ttu-id="1f83a-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f83a-133">OUTPUTS</span></span>

### <span data-ttu-id="1f83a-134">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1f83a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="1f83a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f83a-135">NOTES</span></span>

## <span data-ttu-id="1f83a-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f83a-136">RELATED LINKS</span></span>

[<span data-ttu-id="1f83a-137">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1f83a-137">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="1f83a-138">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1f83a-138">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="1f83a-139">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1f83a-139">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="1f83a-140">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1f83a-140">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="1f83a-141">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1f83a-141">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
