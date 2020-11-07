---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 4c7f4b4f308d04c6f9c82e70f9fbe0598bd4a9fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917686"
---
# <span data-ttu-id="b17e7-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b17e7-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="b17e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b17e7-102">SYNOPSIS</span></span>
<span data-ttu-id="b17e7-103">Ändrar en API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="b17e7-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="b17e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b17e7-104">SYNTAX</span></span>

### <span data-ttu-id="b17e7-105">EventHubLoggerSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b17e7-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b17e7-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="b17e7-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b17e7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b17e7-107">DESCRIPTION</span></span>
<span data-ttu-id="b17e7-108">Cmdleten **set-AzApiManagementLogger** ändrar inställningar för en Azure API Management- **loggning**.</span><span class="sxs-lookup"><span data-stu-id="b17e7-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="b17e7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b17e7-109">EXAMPLES</span></span>

### <span data-ttu-id="b17e7-110">Exempel 1: ändra EventHub-loggning</span><span class="sxs-lookup"><span data-stu-id="b17e7-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="b17e7-111">Det här kommandot ändrar en loggare som har ID-Logger123.</span><span class="sxs-lookup"><span data-stu-id="b17e7-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="b17e7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b17e7-112">PARAMETERS</span></span>

### <span data-ttu-id="b17e7-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="b17e7-113">-ConnectionString</span></span>
<span data-ttu-id="b17e7-114">Anger en anslutnings sträng för Azure Event Hubs som innehåller rättigheter för att skicka principer.</span><span class="sxs-lookup"><span data-stu-id="b17e7-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b17e7-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b17e7-115">-Context</span></span>
<span data-ttu-id="b17e7-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b17e7-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b17e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b17e7-117">-DefaultProfile</span></span>
<span data-ttu-id="b17e7-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b17e7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b17e7-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="b17e7-119">-Description</span></span>
<span data-ttu-id="b17e7-120">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="b17e7-120">Specifies a description.</span></span>

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

### <span data-ttu-id="b17e7-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="b17e7-121">-InstrumentationKey</span></span>
<span data-ttu-id="b17e7-122">Instrumentation-tangenten för program insikter.</span><span class="sxs-lookup"><span data-stu-id="b17e7-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="b17e7-123">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b17e7-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b17e7-124">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="b17e7-124">-IsBuffered</span></span>
<span data-ttu-id="b17e7-125">Anger att posterna i logg filen buffras innan de publiceras.</span><span class="sxs-lookup"><span data-stu-id="b17e7-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="b17e7-126">När posterna buffras skickas de till händelse NAV var 15: e sekund, eller när bufferten tar emot 256 KB av meddelanden.</span><span class="sxs-lookup"><span data-stu-id="b17e7-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b17e7-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="b17e7-127">-LoggerId</span></span>
<span data-ttu-id="b17e7-128">Anger ID för den loggade loggningen.</span><span class="sxs-lookup"><span data-stu-id="b17e7-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="b17e7-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="b17e7-129">-Name</span></span>
<span data-ttu-id="b17e7-130">Anger entitetsnamnet för en händelsehubben från Azure Classic-portalen.</span><span class="sxs-lookup"><span data-stu-id="b17e7-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b17e7-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b17e7-131">-PassThru</span></span>
<span data-ttu-id="b17e7-132">Anger att denna cmdlet returnerar  **PsApiManagementLogger** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="b17e7-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b17e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b17e7-133">CommonParameters</span></span>
<span data-ttu-id="b17e7-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b17e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b17e7-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b17e7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b17e7-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b17e7-136">INPUTS</span></span>

### <span data-ttu-id="b17e7-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b17e7-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b17e7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b17e7-138">System.String</span></span>

### <span data-ttu-id="b17e7-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b17e7-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b17e7-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b17e7-140">OUTPUTS</span></span>

### <span data-ttu-id="b17e7-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b17e7-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="b17e7-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b17e7-142">NOTES</span></span>

## <span data-ttu-id="b17e7-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b17e7-143">RELATED LINKS</span></span>

[<span data-ttu-id="b17e7-144">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b17e7-144">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="b17e7-145">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b17e7-145">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="b17e7-146">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="b17e7-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)


