---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 709e8483a5f21e3afc58add1046b5dae22bea7b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089935"
---
# <span data-ttu-id="428fc-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="428fc-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="428fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="428fc-102">SYNOPSIS</span></span>
<span data-ttu-id="428fc-103">Skapar en instans av PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="428fc-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="428fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="428fc-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="428fc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="428fc-105">DESCRIPTION</span></span>
<span data-ttu-id="428fc-106">Kommandot hjälp för att skapa en instans av PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="428fc-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="428fc-107">Kommandot ska användas med kommandot New-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="428fc-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="428fc-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="428fc-108">EXAMPLES</span></span>

### <span data-ttu-id="428fc-109">Exempel 1: skapa en SSL-inställning för att aktivera TLS 1,0 på både server dels och klient delen</span><span class="sxs-lookup"><span data-stu-id="428fc-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="428fc-110">Skapa en ny instans av PsApiManagementSslSetting för att aktivera TLSv 1,0 i båda klient delen (mellan klient och APIM) och Server delen (mellan APIM och Server delen) för ApiManagement Gateway.</span><span class="sxs-lookup"><span data-stu-id="428fc-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="428fc-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="428fc-111">PARAMETERS</span></span>

### <span data-ttu-id="428fc-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="428fc-112">-BackendProtocol</span></span>
<span data-ttu-id="428fc-113">Säkerhets protokoll inställningar för backend.</span><span class="sxs-lookup"><span data-stu-id="428fc-113">Backend Security protocol settings.</span></span> <span data-ttu-id="428fc-114">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="428fc-114">This parameter is optional.</span></span>
<span data-ttu-id="428fc-115">Giltiga protokoll inställningar är `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="428fc-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="428fc-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="428fc-116">-CipherSuite</span></span>
<span data-ttu-id="428fc-117">Inställningar för SSL-chiffersviter i angiven ordning.</span><span class="sxs-lookup"><span data-stu-id="428fc-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="428fc-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="428fc-118">This parameter is optional.</span></span>
<span data-ttu-id="428fc-119">Giltiga inställningar är `TripleDes168` -Aktivera/inaktivera rese-Des 168</span><span class="sxs-lookup"><span data-stu-id="428fc-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="428fc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428fc-120">-DefaultProfile</span></span>
<span data-ttu-id="428fc-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="428fc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="428fc-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="428fc-122">-FrontendProtocol</span></span>
<span data-ttu-id="428fc-123">Inställningar för säkerhets protokoll för klient delen.</span><span class="sxs-lookup"><span data-stu-id="428fc-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="428fc-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="428fc-124">This parameter is optional.</span></span>
<span data-ttu-id="428fc-125">Giltiga protokoll inställningar är `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="428fc-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="428fc-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="428fc-126">-ServerProtocol</span></span>
<span data-ttu-id="428fc-127">Server protokoll inställningar som Http2.</span><span class="sxs-lookup"><span data-stu-id="428fc-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="428fc-128">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="428fc-128">This parameter is optional.</span></span>
<span data-ttu-id="428fc-129">Giltiga inställningar är `Http2` -Aktivera Http 2,0</span><span class="sxs-lookup"><span data-stu-id="428fc-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="428fc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428fc-130">CommonParameters</span></span>
<span data-ttu-id="428fc-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="428fc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428fc-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="428fc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428fc-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="428fc-133">INPUTS</span></span>

### <span data-ttu-id="428fc-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="428fc-134">None</span></span>

## <span data-ttu-id="428fc-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="428fc-135">OUTPUTS</span></span>

### <span data-ttu-id="428fc-136">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="428fc-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="428fc-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="428fc-137">NOTES</span></span>

## <span data-ttu-id="428fc-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="428fc-138">RELATED LINKS</span></span>

[<span data-ttu-id="428fc-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="428fc-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

