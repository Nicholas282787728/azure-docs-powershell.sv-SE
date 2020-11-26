---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: c4b7246a2b600c1ed0d9f8a01ea3fd69cd4af33d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269513"
---
# <span data-ttu-id="30f60-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="30f60-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="30f60-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30f60-102">SYNOPSIS</span></span>
<span data-ttu-id="30f60-103">Hämtar gränssnitts objekt för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="30f60-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="30f60-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30f60-104">SYNTAX</span></span>

### <span data-ttu-id="30f60-105">GetAllLoggers (standard)</span><span class="sxs-lookup"><span data-stu-id="30f60-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30f60-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="30f60-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30f60-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30f60-107">DESCRIPTION</span></span>
<span data-ttu-id="30f60-108">Cmdleten **Get-AzApiManagementLogger** får en Azure API Management- **loggning** eller alla loggar.</span><span class="sxs-lookup"><span data-stu-id="30f60-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="30f60-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30f60-109">EXAMPLES</span></span>

### <span data-ttu-id="30f60-110">Exempel 1: Hämta alla loggar</span><span class="sxs-lookup"><span data-stu-id="30f60-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="30f60-111">Det här kommandot får alla loggar för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="30f60-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="30f60-112">Exempel 2: skaffa en särskild loggning</span><span class="sxs-lookup"><span data-stu-id="30f60-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="30f60-113">Det här kommandot tar bort en loggare som har ID-Logger123.</span><span class="sxs-lookup"><span data-stu-id="30f60-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="30f60-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30f60-114">PARAMETERS</span></span>

### <span data-ttu-id="30f60-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="30f60-115">-Context</span></span>
<span data-ttu-id="30f60-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="30f60-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="30f60-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f60-117">-DefaultProfile</span></span>
<span data-ttu-id="30f60-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30f60-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30f60-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="30f60-119">-LoggerId</span></span>
<span data-ttu-id="30f60-120">Anger ID för den specifika logg filen som ska visas.</span><span class="sxs-lookup"><span data-stu-id="30f60-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByLoggerId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30f60-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f60-121">CommonParameters</span></span>
<span data-ttu-id="30f60-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30f60-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f60-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30f60-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f60-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30f60-124">INPUTS</span></span>

### <span data-ttu-id="30f60-125">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="30f60-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="30f60-126">System. String</span><span class="sxs-lookup"><span data-stu-id="30f60-126">System.String</span></span>

## <span data-ttu-id="30f60-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30f60-127">OUTPUTS</span></span>

### <span data-ttu-id="30f60-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="30f60-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="30f60-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30f60-129">NOTES</span></span>

## <span data-ttu-id="30f60-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30f60-130">RELATED LINKS</span></span>

[<span data-ttu-id="30f60-131">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="30f60-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="30f60-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="30f60-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="30f60-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="30f60-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)

