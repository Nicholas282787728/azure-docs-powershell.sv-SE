---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: c7827f0df8b1baf4bb2fead9df091619751c969c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578624"
---
# <span data-ttu-id="d21bb-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d21bb-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="d21bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d21bb-102">SYNOPSIS</span></span>
<span data-ttu-id="d21bb-103">Skapar en API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="d21bb-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d21bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d21bb-104">SYNTAX</span></span>

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d21bb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d21bb-105">DESCRIPTION</span></span>
<span data-ttu-id="d21bb-106">Cmdleten **New-AzureRmApiManagementLogger** skapar en Azure API Management- **loggning**.</span><span class="sxs-lookup"><span data-stu-id="d21bb-106">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="d21bb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d21bb-107">EXAMPLES</span></span>

### <span data-ttu-id="d21bb-108">Exempel 1: skapa en loggare</span><span class="sxs-lookup"><span data-stu-id="d21bb-108">Example 1: Create a logger</span></span>
```
PS C:\>New-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="d21bb-109">Det här kommandot skapar en loggare som heter ContosoSdkEventHub genom att använda den angivna anslutnings strängen.</span><span class="sxs-lookup"><span data-stu-id="d21bb-109">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="d21bb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d21bb-110">PARAMETERS</span></span>

### <span data-ttu-id="d21bb-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d21bb-111">-ConnectionString</span></span>
<span data-ttu-id="d21bb-112">Anger en anslutnings sträng för Azure Event Hubs som börjar med följande:</span><span class="sxs-lookup"><span data-stu-id="d21bb-112">Specifies an Azure Event Hubs connection string that starts with the following:</span></span> 

`Endpoint=endpoint and key from Azure classic portal`

<span data-ttu-id="d21bb-113">Du måste konfigurera knappen för att skicka rättigheter i anslutnings strängen.</span><span class="sxs-lookup"><span data-stu-id="d21bb-113">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d21bb-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d21bb-114">-Context</span></span>
<span data-ttu-id="d21bb-115">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d21bb-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d21bb-116">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d21bb-116">-Description</span></span>
<span data-ttu-id="d21bb-117">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="d21bb-117">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d21bb-118">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="d21bb-118">-IsBuffered</span></span>
<span data-ttu-id="d21bb-119">Anger om posterna i logg filen buffras före publicering.</span><span class="sxs-lookup"><span data-stu-id="d21bb-119">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="d21bb-120">Standardvärdet är $True.</span><span class="sxs-lookup"><span data-stu-id="d21bb-120">The default value is $True.</span></span>
<span data-ttu-id="d21bb-121">När posterna buffras skickas de till händelse NAV var 15: e sekund, eller när bufferten tar emot 256 KB av meddelanden.</span><span class="sxs-lookup"><span data-stu-id="d21bb-121">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d21bb-122">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="d21bb-122">-LoggerId</span></span>
<span data-ttu-id="d21bb-123">Anger ett ID för loggningen.</span><span class="sxs-lookup"><span data-stu-id="d21bb-123">Specifies an ID for the logger.</span></span>
<span data-ttu-id="d21bb-124">Om du inte anger något ID skapar den här cmdleten en.</span><span class="sxs-lookup"><span data-stu-id="d21bb-124">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d21bb-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="d21bb-125">-Name</span></span>
<span data-ttu-id="d21bb-126">Anger entitetsnamnet för en händelsehubben från Azure Classic-portalen.</span><span class="sxs-lookup"><span data-stu-id="d21bb-126">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d21bb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d21bb-127">-DefaultProfile</span></span>
<span data-ttu-id="d21bb-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d21bb-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d21bb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d21bb-129">CommonParameters</span></span>
<span data-ttu-id="d21bb-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d21bb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d21bb-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d21bb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d21bb-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d21bb-132">INPUTS</span></span>

## <span data-ttu-id="d21bb-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d21bb-133">OUTPUTS</span></span>

### <span data-ttu-id="d21bb-134">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d21bb-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="d21bb-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d21bb-135">NOTES</span></span>

## <span data-ttu-id="d21bb-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d21bb-136">RELATED LINKS</span></span>

[<span data-ttu-id="d21bb-137">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d21bb-137">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="d21bb-138">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d21bb-138">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="d21bb-139">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="d21bb-139">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


