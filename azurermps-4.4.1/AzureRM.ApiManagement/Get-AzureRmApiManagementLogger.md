---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: 48033c250286c59e2cadfadc1a5b5d28f869a66c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581559"
---
# <span data-ttu-id="d06a2-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d06a2-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="d06a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d06a2-102">SYNOPSIS</span></span>
<span data-ttu-id="d06a2-103">Hämtar gränssnitts objekt för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="d06a2-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d06a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d06a2-104">SYNTAX</span></span>

### <span data-ttu-id="d06a2-105">Hämta alla loggar (standard)</span><span class="sxs-lookup"><span data-stu-id="d06a2-105">Get all loggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d06a2-106">Hämta efter loggar-ID</span><span class="sxs-lookup"><span data-stu-id="d06a2-106">Get by logger ID</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d06a2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d06a2-107">DESCRIPTION</span></span>
<span data-ttu-id="d06a2-108">Cmdleten **Get-AzureRmApiManagementLogger** får en Azure API Management- **loggning** eller alla loggar.</span><span class="sxs-lookup"><span data-stu-id="d06a2-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="d06a2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d06a2-109">EXAMPLES</span></span>

### <span data-ttu-id="d06a2-110">Exempel 1: Hämta alla loggar</span><span class="sxs-lookup"><span data-stu-id="d06a2-110">Example 1: Get all loggers</span></span>
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext
```

<span data-ttu-id="d06a2-111">Det här kommandot får alla loggar för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="d06a2-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="d06a2-112">Exempel 2: skaffa en särskild loggning</span><span class="sxs-lookup"><span data-stu-id="d06a2-112">Example 2: Get a specific logger</span></span>
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123"
```

<span data-ttu-id="d06a2-113">Det här kommandot tar bort en loggare som har ID-Logger123.</span><span class="sxs-lookup"><span data-stu-id="d06a2-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="d06a2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d06a2-114">PARAMETERS</span></span>

### <span data-ttu-id="d06a2-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d06a2-115">-Context</span></span>
<span data-ttu-id="d06a2-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d06a2-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d06a2-117">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="d06a2-117">-LoggerId</span></span>
<span data-ttu-id="d06a2-118">Anger ID för den specifika logg filen som ska visas.</span><span class="sxs-lookup"><span data-stu-id="d06a2-118">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by logger ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d06a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d06a2-119">-DefaultProfile</span></span>
<span data-ttu-id="d06a2-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d06a2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d06a2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d06a2-121">CommonParameters</span></span>
<span data-ttu-id="d06a2-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d06a2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d06a2-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d06a2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d06a2-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d06a2-124">INPUTS</span></span>

## <span data-ttu-id="d06a2-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d06a2-125">OUTPUTS</span></span>

### <span data-ttu-id="d06a2-126">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger></span><span class="sxs-lookup"><span data-stu-id="d06a2-126">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger></span></span>

## <span data-ttu-id="d06a2-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d06a2-127">NOTES</span></span>

## <span data-ttu-id="d06a2-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d06a2-128">RELATED LINKS</span></span>

[<span data-ttu-id="d06a2-129">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d06a2-129">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="d06a2-130">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d06a2-130">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="d06a2-131">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d06a2-131">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


