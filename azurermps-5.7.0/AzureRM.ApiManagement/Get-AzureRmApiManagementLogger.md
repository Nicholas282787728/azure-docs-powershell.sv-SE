---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: bcfcd052d2278fa39bc310a5c1927457a1b0fcd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581208"
---
# <span data-ttu-id="8d2c6-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8d2c6-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="8d2c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d2c6-102">SYNOPSIS</span></span>
<span data-ttu-id="8d2c6-103">Hämtar gränssnitts objekt för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="8d2c6-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d2c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d2c6-104">SYNTAX</span></span>

### <span data-ttu-id="8d2c6-105">GetAllLoggers (standard)</span><span class="sxs-lookup"><span data-stu-id="8d2c6-105">GetAllLoggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d2c6-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="8d2c6-106">GetByLoggerId</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d2c6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d2c6-107">DESCRIPTION</span></span>
<span data-ttu-id="8d2c6-108">Cmdleten **Get-AzureRmApiManagementLogger** får en Azure API Management- **loggning** eller alla loggar.</span><span class="sxs-lookup"><span data-stu-id="8d2c6-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="8d2c6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d2c6-109">EXAMPLES</span></span>

### <span data-ttu-id="8d2c6-110">Exempel 1: Hämta alla loggar</span><span class="sxs-lookup"><span data-stu-id="8d2c6-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext
```

<span data-ttu-id="8d2c6-111">Det här kommandot får alla loggar för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="8d2c6-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="8d2c6-112">Exempel 2: skaffa en särskild loggning</span><span class="sxs-lookup"><span data-stu-id="8d2c6-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="8d2c6-113">Det här kommandot tar bort en loggare som har ID-Logger123.</span><span class="sxs-lookup"><span data-stu-id="8d2c6-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="8d2c6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d2c6-114">PARAMETERS</span></span>

### <span data-ttu-id="8d2c6-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="8d2c6-115">-Context</span></span>
<span data-ttu-id="8d2c6-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8d2c6-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d2c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d2c6-117">-DefaultProfile</span></span>
<span data-ttu-id="8d2c6-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d2c6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2c6-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="8d2c6-119">-LoggerId</span></span>
<span data-ttu-id="8d2c6-120">Anger ID för den specifika logg filen som ska visas.</span><span class="sxs-lookup"><span data-stu-id="8d2c6-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByLoggerId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d2c6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d2c6-121">CommonParameters</span></span>
<span data-ttu-id="8d2c6-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d2c6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d2c6-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d2c6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d2c6-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d2c6-124">INPUTS</span></span>

### <span data-ttu-id="8d2c6-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="8d2c6-125">None</span></span>
<span data-ttu-id="8d2c6-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="8d2c6-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8d2c6-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d2c6-127">OUTPUTS</span></span>

### <span data-ttu-id="8d2c6-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8d2c6-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>
<span data-ttu-id="8d2c6-129">Detaljerna för loggningen konfigurerad i API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="8d2c6-129">The detail of the Logger configured in API Management service.</span></span>

### <span data-ttu-id="8d2c6-130">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger></span><span class="sxs-lookup"><span data-stu-id="8d2c6-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger></span></span>
<span data-ttu-id="8d2c6-131">Listan över loggar konfigurerade i API Management Service.</span><span class="sxs-lookup"><span data-stu-id="8d2c6-131">The list of Loggers configured in API Management service.</span></span>

## <span data-ttu-id="8d2c6-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d2c6-132">NOTES</span></span>

## <span data-ttu-id="8d2c6-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d2c6-133">RELATED LINKS</span></span>

[<span data-ttu-id="8d2c6-134">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8d2c6-134">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="8d2c6-135">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8d2c6-135">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="8d2c6-136">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8d2c6-136">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)

