---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
ms.openlocfilehash: c1ddf2ec1e83a73d130f5be5eee38bfc8cac4c9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745765"
---
# <span data-ttu-id="e4219-101">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e4219-101">New-AzApiManagementLogger</span></span>

## <span data-ttu-id="e4219-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4219-102">SYNOPSIS</span></span>
<span data-ttu-id="e4219-103">Skapar en API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="e4219-103">Creates an API Management Logger.</span></span>

## <span data-ttu-id="e4219-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4219-104">SYNTAX</span></span>

### <span data-ttu-id="e4219-105">EventHubLoggerSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e4219-105">EventHubLoggerSet (Default)</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4219-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="e4219-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -InstrumentationKey <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4219-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4219-107">DESCRIPTION</span></span>
<span data-ttu-id="e4219-108">Cmdleten **New-AzApiManagementLogger** skapar en Azure API Management- **loggning**.</span><span class="sxs-lookup"><span data-stu-id="e4219-108">The **New-AzApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="e4219-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4219-109">EXAMPLES</span></span>

### <span data-ttu-id="e4219-110">Exempel 1: skapa en loggare</span><span class="sxs-lookup"><span data-stu-id="e4219-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="e4219-111">Det här kommandot skapar en loggare som heter ContosoSdkEventHub genom att använda den angivna anslutnings strängen.</span><span class="sxs-lookup"><span data-stu-id="e4219-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="e4219-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4219-112">PARAMETERS</span></span>

### <span data-ttu-id="e4219-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e4219-113">-ConnectionString</span></span>
<span data-ttu-id="e4219-114">Anger en anslutnings sträng för Azure Event Hubs som börjar med följande: `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="e4219-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="e4219-115">Du måste konfigurera knappen för att skicka rättigheter i anslutnings strängen.</span><span class="sxs-lookup"><span data-stu-id="e4219-115">The Key with Send Rights in the connection string must be configured.</span></span>

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

### <span data-ttu-id="e4219-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e4219-116">-Context</span></span>
<span data-ttu-id="e4219-117">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e4219-117">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4219-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4219-118">-DefaultProfile</span></span>
<span data-ttu-id="e4219-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4219-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4219-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="e4219-120">-Description</span></span>
<span data-ttu-id="e4219-121">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="e4219-121">Specifies a description.</span></span>

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

### <span data-ttu-id="e4219-122">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="e4219-122">-InstrumentationKey</span></span>
<span data-ttu-id="e4219-123">Instrumentation-tangenten för program insikter.</span><span class="sxs-lookup"><span data-stu-id="e4219-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="e4219-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="e4219-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="e4219-125">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="e4219-125">-IsBuffered</span></span>
<span data-ttu-id="e4219-126">Anger om posterna i logg filen buffras före publicering.</span><span class="sxs-lookup"><span data-stu-id="e4219-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="e4219-127">Standardvärdet är $True.</span><span class="sxs-lookup"><span data-stu-id="e4219-127">The default value is $True.</span></span>
<span data-ttu-id="e4219-128">När posterna buffras skickas de till händelse NAV var 15: e sekund, eller när bufferten tar emot 256 KB av meddelanden.</span><span class="sxs-lookup"><span data-stu-id="e4219-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="e4219-129">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="e4219-129">-LoggerId</span></span>
<span data-ttu-id="e4219-130">Anger ett ID för loggningen.</span><span class="sxs-lookup"><span data-stu-id="e4219-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="e4219-131">Om du inte anger något ID skapar den här cmdleten en.</span><span class="sxs-lookup"><span data-stu-id="e4219-131">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="e4219-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="e4219-132">-Name</span></span>
<span data-ttu-id="e4219-133">Anger entitetsnamnet för en händelsehubben från Azure Classic-portalen.</span><span class="sxs-lookup"><span data-stu-id="e4219-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="e4219-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4219-134">CommonParameters</span></span>
<span data-ttu-id="e4219-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4219-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4219-136">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4219-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4219-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4219-137">INPUTS</span></span>

### <span data-ttu-id="e4219-138">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e4219-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e4219-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e4219-139">System.String</span></span>

### <span data-ttu-id="e4219-140">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e4219-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e4219-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4219-141">OUTPUTS</span></span>

### <span data-ttu-id="e4219-142">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e4219-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="e4219-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4219-143">NOTES</span></span>

## <span data-ttu-id="e4219-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4219-144">RELATED LINKS</span></span>

[<span data-ttu-id="e4219-145">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e4219-145">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="e4219-146">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e4219-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="e4219-147">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e4219-147">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)

