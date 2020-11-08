---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261491"
---
# <span data-ttu-id="6aa22-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="6aa22-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="6aa22-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6aa22-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa22-103">Skapar en instans av PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="6aa22-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="6aa22-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6aa22-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6aa22-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6aa22-105">DESCRIPTION</span></span>
<span data-ttu-id="6aa22-106">Kommandot hjälp för att skapa en instans av PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="6aa22-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="6aa22-107">Kommandot ska användas med kommandot New-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6aa22-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="6aa22-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6aa22-108">EXAMPLES</span></span>

### <span data-ttu-id="6aa22-109">Exempel 1: skapa en SSL-inställning för att aktivera TLS 1,0 på både server dels och klient delen</span><span class="sxs-lookup"><span data-stu-id="6aa22-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="6aa22-110">Skapa en ny instans av PsApiManagementSslSetting för att aktivera TLSv 1,0 i båda klient delen (mellan klient och APIM) och Server delen (mellan APIM och Server delen) för ApiManagement Gateway.</span><span class="sxs-lookup"><span data-stu-id="6aa22-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="6aa22-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6aa22-111">PARAMETERS</span></span>

### <span data-ttu-id="6aa22-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="6aa22-112">-BackendProtocol</span></span>
<span data-ttu-id="6aa22-113">Säkerhets protokoll inställningar för backend.</span><span class="sxs-lookup"><span data-stu-id="6aa22-113">Backend Security protocol settings.</span></span> <span data-ttu-id="6aa22-114">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="6aa22-114">This parameter is optional.</span></span>
<span data-ttu-id="6aa22-115">Giltiga protokoll inställningar är `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="6aa22-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="6aa22-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="6aa22-116">-CipherSuite</span></span>
<span data-ttu-id="6aa22-117">Inställningar för SSL-chiffersviter i angiven ordning.</span><span class="sxs-lookup"><span data-stu-id="6aa22-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="6aa22-118">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="6aa22-118">This parameter is optional.</span></span>
<span data-ttu-id="6aa22-119">Giltiga inställningar är `TripleDes168` -Aktivera/inaktivera rese-Des 168</span><span class="sxs-lookup"><span data-stu-id="6aa22-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="6aa22-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa22-120">-DefaultProfile</span></span>
<span data-ttu-id="6aa22-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa22-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aa22-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="6aa22-122">-FrontendProtocol</span></span>
<span data-ttu-id="6aa22-123">Inställningar för säkerhets protokoll för klient delen.</span><span class="sxs-lookup"><span data-stu-id="6aa22-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="6aa22-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="6aa22-124">This parameter is optional.</span></span>
<span data-ttu-id="6aa22-125">Giltiga protokoll inställningar är `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="6aa22-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="6aa22-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="6aa22-126">-ServerProtocol</span></span>
<span data-ttu-id="6aa22-127">Server protokoll inställningar som Http2.</span><span class="sxs-lookup"><span data-stu-id="6aa22-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="6aa22-128">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="6aa22-128">This parameter is optional.</span></span>
<span data-ttu-id="6aa22-129">Giltiga inställningar är `Http2` -Aktivera Http 2,0</span><span class="sxs-lookup"><span data-stu-id="6aa22-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="6aa22-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa22-130">CommonParameters</span></span>
<span data-ttu-id="6aa22-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aa22-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa22-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6aa22-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa22-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6aa22-133">INPUTS</span></span>

### <span data-ttu-id="6aa22-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="6aa22-134">None</span></span>

## <span data-ttu-id="6aa22-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6aa22-135">OUTPUTS</span></span>

### <span data-ttu-id="6aa22-136">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="6aa22-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="6aa22-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6aa22-137">NOTES</span></span>

## <span data-ttu-id="6aa22-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6aa22-138">RELATED LINKS</span></span>

[<span data-ttu-id="6aa22-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6aa22-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

