---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 7c4fb7c2147d7daf3307c2895893198ebe805ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745749"
---
# <span data-ttu-id="8a393-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="8a393-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="8a393-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a393-102">SYNOPSIS</span></span>
<span data-ttu-id="8a393-103">Skapar en instans av PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="8a393-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="8a393-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a393-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a393-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a393-105">DESCRIPTION</span></span>
<span data-ttu-id="8a393-106">Kommandot hjälp för att skapa en instans av PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="8a393-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="8a393-107">Kommandot ska användas med kommandot New-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8a393-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="8a393-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a393-108">EXAMPLES</span></span>

### <span data-ttu-id="8a393-109">Exempel 1: skapa en SSL-inställning för att aktivera TLS 1,0 på både server dels och klient delen</span><span class="sxs-lookup"><span data-stu-id="8a393-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="8a393-110">Skapa en ny instans av PsApiManagementSslSetting för att aktivera TLSv 1,0 i båda klient delen (mellan klient och APIM) och Server delen (mellan APIM och Server delen) för ApiManagement Gateway.</span><span class="sxs-lookup"><span data-stu-id="8a393-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="8a393-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a393-111">PARAMETERS</span></span>

### <span data-ttu-id="8a393-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="8a393-112">-BackendProtocol</span></span>
<span data-ttu-id="8a393-113">Säkerhets protokoll inställningar för backend.</span><span class="sxs-lookup"><span data-stu-id="8a393-113">Backend Security protocol settings.</span></span> <span data-ttu-id="8a393-114">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="8a393-114">This parameter is optional.</span></span>

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

### <span data-ttu-id="8a393-115">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="8a393-115">-CipherSuite</span></span>
<span data-ttu-id="8a393-116">Inställningar för SSL-chiffersviter i angiven ordning.</span><span class="sxs-lookup"><span data-stu-id="8a393-116">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="8a393-117">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="8a393-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="8a393-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a393-118">-DefaultProfile</span></span>
<span data-ttu-id="8a393-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a393-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a393-120">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="8a393-120">-FrontendProtocol</span></span>
<span data-ttu-id="8a393-121">Inställningar för säkerhets protokoll för klient delen.</span><span class="sxs-lookup"><span data-stu-id="8a393-121">Frontend Security protocols settings.</span></span> <span data-ttu-id="8a393-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="8a393-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="8a393-123">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="8a393-123">-ServerProtocol</span></span>
<span data-ttu-id="8a393-124">Server protokoll inställningar som Http2.</span><span class="sxs-lookup"><span data-stu-id="8a393-124">Server protocol settings like Http2.</span></span> <span data-ttu-id="8a393-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="8a393-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="8a393-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a393-126">CommonParameters</span></span>
<span data-ttu-id="8a393-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a393-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a393-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a393-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a393-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a393-129">INPUTS</span></span>

### <span data-ttu-id="8a393-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="8a393-130">None</span></span>

## <span data-ttu-id="8a393-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a393-131">OUTPUTS</span></span>

### <span data-ttu-id="8a393-132">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="8a393-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="8a393-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a393-133">NOTES</span></span>

## <span data-ttu-id="8a393-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a393-134">RELATED LINKS</span></span>

[<span data-ttu-id="8a393-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8a393-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

