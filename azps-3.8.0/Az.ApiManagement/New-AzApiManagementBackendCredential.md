---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: c1495c505653470f4aa6b818162d57e02893c5e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089985"
---
# <span data-ttu-id="e30d1-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e30d1-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="e30d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e30d1-102">SYNOPSIS</span></span>
<span data-ttu-id="e30d1-103">Skapar ett nytt kontrakt för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="e30d1-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="e30d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e30d1-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e30d1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e30d1-105">DESCRIPTION</span></span>
<span data-ttu-id="e30d1-106">Skapar ett nytt kontrakt för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="e30d1-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="e30d1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e30d1-107">EXAMPLES</span></span>

### <span data-ttu-id="e30d1-108">Skapa en server dels referenser In-Memory objekt</span><span class="sxs-lookup"><span data-stu-id="e30d1-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="e30d1-109">Skapar ett kontrakt för inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="e30d1-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="e30d1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e30d1-110">PARAMETERS</span></span>

### <span data-ttu-id="e30d1-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="e30d1-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="e30d1-112">Huvud tillstånd som används för Server delen.</span><span class="sxs-lookup"><span data-stu-id="e30d1-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="e30d1-113">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e30d1-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="e30d1-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="e30d1-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="e30d1-115">Godkännande schema som används för Server delen.</span><span class="sxs-lookup"><span data-stu-id="e30d1-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="e30d1-116">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e30d1-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="e30d1-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e30d1-117">-CertificateThumbprint</span></span>
<span data-ttu-id="e30d1-118">Thumbprints för klient certifikat.</span><span class="sxs-lookup"><span data-stu-id="e30d1-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="e30d1-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e30d1-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="e30d1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e30d1-120">-DefaultProfile</span></span>
<span data-ttu-id="e30d1-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e30d1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e30d1-122">-Rubrik</span><span class="sxs-lookup"><span data-stu-id="e30d1-122">-Header</span></span>
<span data-ttu-id="e30d1-123">Rubrik parameter värden som accepteras av Server delen.</span><span class="sxs-lookup"><span data-stu-id="e30d1-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="e30d1-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e30d1-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="e30d1-125">-Fråga</span><span class="sxs-lookup"><span data-stu-id="e30d1-125">-Query</span></span>
<span data-ttu-id="e30d1-126">Parameter värden för frågor som accepteras av Server delen.</span><span class="sxs-lookup"><span data-stu-id="e30d1-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="e30d1-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e30d1-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="e30d1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30d1-128">CommonParameters</span></span>
<span data-ttu-id="e30d1-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e30d1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30d1-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e30d1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30d1-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e30d1-131">INPUTS</span></span>

### <span data-ttu-id="e30d1-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="e30d1-132">None</span></span>

## <span data-ttu-id="e30d1-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e30d1-133">OUTPUTS</span></span>

### <span data-ttu-id="e30d1-134">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e30d1-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="e30d1-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e30d1-135">NOTES</span></span>

## <span data-ttu-id="e30d1-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e30d1-136">RELATED LINKS</span></span>

[<span data-ttu-id="e30d1-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e30d1-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="e30d1-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e30d1-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="e30d1-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e30d1-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="e30d1-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e30d1-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="e30d1-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e30d1-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
