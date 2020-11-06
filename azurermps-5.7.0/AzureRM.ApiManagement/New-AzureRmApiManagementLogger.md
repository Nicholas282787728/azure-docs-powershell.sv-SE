---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: 2929cbd89328d971b47b748d4aa042ade13c1af9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576642"
---
# <span data-ttu-id="188e5-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="188e5-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="188e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="188e5-102">SYNOPSIS</span></span>
<span data-ttu-id="188e5-103">Skapar en API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="188e5-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="188e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="188e5-104">SYNTAX</span></span>

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="188e5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="188e5-105">DESCRIPTION</span></span>
<span data-ttu-id="188e5-106">Cmdleten **New-AzureRmApiManagementLogger** skapar en Azure API Management- **loggning**.</span><span class="sxs-lookup"><span data-stu-id="188e5-106">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="188e5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="188e5-107">EXAMPLES</span></span>

### <span data-ttu-id="188e5-108">Exempel 1: skapa en loggare</span><span class="sxs-lookup"><span data-stu-id="188e5-108">Example 1: Create a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="188e5-109">Det här kommandot skapar en loggare som heter ContosoSdkEventHub genom att använda den angivna anslutnings strängen.</span><span class="sxs-lookup"><span data-stu-id="188e5-109">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="188e5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="188e5-110">PARAMETERS</span></span>

### <span data-ttu-id="188e5-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="188e5-111">-ConnectionString</span></span>
<span data-ttu-id="188e5-112">Anger en anslutnings sträng för Azure Event Hubs som börjar med följande:</span><span class="sxs-lookup"><span data-stu-id="188e5-112">Specifies an Azure Event Hubs connection string that starts with the following:</span></span> 

`Endpoint=endpoint and key from Azure classic portal`

<span data-ttu-id="188e5-113">Du måste konfigurera knappen för att skicka rättigheter i anslutnings strängen.</span><span class="sxs-lookup"><span data-stu-id="188e5-113">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="188e5-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="188e5-114">-Context</span></span>
<span data-ttu-id="188e5-115">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="188e5-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="188e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="188e5-116">-DefaultProfile</span></span>
<span data-ttu-id="188e5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="188e5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="188e5-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="188e5-118">-Description</span></span>
<span data-ttu-id="188e5-119">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="188e5-119">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="188e5-120">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="188e5-120">-IsBuffered</span></span>
<span data-ttu-id="188e5-121">Anger om posterna i logg filen buffras före publicering.</span><span class="sxs-lookup"><span data-stu-id="188e5-121">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="188e5-122">Standardvärdet är $True.</span><span class="sxs-lookup"><span data-stu-id="188e5-122">The default value is $True.</span></span>
<span data-ttu-id="188e5-123">När posterna buffras skickas de till händelse NAV var 15: e sekund, eller när bufferten tar emot 256 KB av meddelanden.</span><span class="sxs-lookup"><span data-stu-id="188e5-123">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="188e5-124">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="188e5-124">-LoggerId</span></span>
<span data-ttu-id="188e5-125">Anger ett ID för loggningen.</span><span class="sxs-lookup"><span data-stu-id="188e5-125">Specifies an ID for the logger.</span></span>
<span data-ttu-id="188e5-126">Om du inte anger något ID skapar den här cmdleten en.</span><span class="sxs-lookup"><span data-stu-id="188e5-126">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="188e5-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="188e5-127">-Name</span></span>
<span data-ttu-id="188e5-128">Anger entitetsnamnet för en händelsehubben från Azure Classic-portalen.</span><span class="sxs-lookup"><span data-stu-id="188e5-128">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="188e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="188e5-129">CommonParameters</span></span>
<span data-ttu-id="188e5-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="188e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="188e5-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="188e5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="188e5-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="188e5-132">INPUTS</span></span>

### <span data-ttu-id="188e5-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="188e5-133">None</span></span>
<span data-ttu-id="188e5-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="188e5-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="188e5-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="188e5-135">OUTPUTS</span></span>

### <span data-ttu-id="188e5-136">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="188e5-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="188e5-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="188e5-137">NOTES</span></span>

## <span data-ttu-id="188e5-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="188e5-138">RELATED LINKS</span></span>

[<span data-ttu-id="188e5-139">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="188e5-139">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="188e5-140">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="188e5-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="188e5-141">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="188e5-141">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


