---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: 04119d70f1cf3ae01b1d74e24cb2e030eecaa46b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755225"
---
# <span data-ttu-id="c32c4-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c32c4-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="c32c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c32c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c32c4-103">Skapar en API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="c32c4-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c32c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c32c4-104">SYNTAX</span></span>

### <span data-ttu-id="c32c4-105">EventHubLoggerSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c32c4-105">EventHubLoggerSet (Default)</span></span>
```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c32c4-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="c32c4-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>]
 -InstrumentationKey <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c32c4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c32c4-107">DESCRIPTION</span></span>
<span data-ttu-id="c32c4-108">Cmdleten **New-AzureRmApiManagementLogger** skapar en Azure API Management- **loggning**.</span><span class="sxs-lookup"><span data-stu-id="c32c4-108">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="c32c4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c32c4-109">EXAMPLES</span></span>

### <span data-ttu-id="c32c4-110">Exempel 1: skapa en loggare</span><span class="sxs-lookup"><span data-stu-id="c32c4-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="c32c4-111">Det här kommandot skapar en loggare som heter ContosoSdkEventHub genom att använda den angivna anslutnings strängen.</span><span class="sxs-lookup"><span data-stu-id="c32c4-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="c32c4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c32c4-112">PARAMETERS</span></span>

### <span data-ttu-id="c32c4-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c32c4-113">-ConnectionString</span></span>
<span data-ttu-id="c32c4-114">Anger en anslutnings sträng för Azure Event Hubs som börjar med följande: `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="c32c4-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="c32c4-115">Du måste konfigurera knappen för att skicka rättigheter i anslutnings strängen.</span><span class="sxs-lookup"><span data-stu-id="c32c4-115">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c32c4-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c32c4-116">-Context</span></span>
<span data-ttu-id="c32c4-117">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c32c4-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c32c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c32c4-118">-DefaultProfile</span></span>
<span data-ttu-id="c32c4-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c32c4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c32c4-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c32c4-120">-Description</span></span>
<span data-ttu-id="c32c4-121">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="c32c4-121">Specifies a description.</span></span>

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

### <span data-ttu-id="c32c4-122">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="c32c4-122">-InstrumentationKey</span></span>
<span data-ttu-id="c32c4-123">Instrumentation-tangenten för program insikter.</span><span class="sxs-lookup"><span data-stu-id="c32c4-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="c32c4-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c32c4-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c32c4-125">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="c32c4-125">-IsBuffered</span></span>
<span data-ttu-id="c32c4-126">Anger om posterna i logg filen buffras före publicering.</span><span class="sxs-lookup"><span data-stu-id="c32c4-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="c32c4-127">Standardvärdet är $True.</span><span class="sxs-lookup"><span data-stu-id="c32c4-127">The default value is $True.</span></span>
<span data-ttu-id="c32c4-128">När posterna buffras skickas de till händelse NAV var 15: e sekund, eller när bufferten tar emot 256 KB av meddelanden.</span><span class="sxs-lookup"><span data-stu-id="c32c4-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c32c4-129">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="c32c4-129">-LoggerId</span></span>
<span data-ttu-id="c32c4-130">Anger ett ID för loggningen.</span><span class="sxs-lookup"><span data-stu-id="c32c4-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="c32c4-131">Om du inte anger något ID skapar den här cmdleten en.</span><span class="sxs-lookup"><span data-stu-id="c32c4-131">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="c32c4-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="c32c4-132">-Name</span></span>
<span data-ttu-id="c32c4-133">Anger entitetsnamnet för en händelsehubben från Azure Classic-portalen.</span><span class="sxs-lookup"><span data-stu-id="c32c4-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c32c4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c32c4-134">CommonParameters</span></span>
<span data-ttu-id="c32c4-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c32c4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c32c4-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c32c4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c32c4-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c32c4-137">INPUTS</span></span>

### <span data-ttu-id="c32c4-138">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c32c4-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c32c4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c32c4-139">System.String</span></span>

### <span data-ttu-id="c32c4-140">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c32c4-140">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c32c4-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c32c4-141">OUTPUTS</span></span>

### <span data-ttu-id="c32c4-142">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c32c4-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="c32c4-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c32c4-143">NOTES</span></span>

## <span data-ttu-id="c32c4-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c32c4-144">RELATED LINKS</span></span>

[<span data-ttu-id="c32c4-145">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c32c4-145">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="c32c4-146">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c32c4-146">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="c32c4-147">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c32c4-147">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


