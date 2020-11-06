---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 7a037b107f3d72a000c2f69c8de507a4f414e283
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576347"
---
# <span data-ttu-id="90f92-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="90f92-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="90f92-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90f92-102">SYNOPSIS</span></span>
<span data-ttu-id="90f92-103">Ändrar en API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="90f92-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90f92-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90f92-104">SYNTAX</span></span>

### <span data-ttu-id="90f92-105">EventHubLoggerSet (standard)</span><span class="sxs-lookup"><span data-stu-id="90f92-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90f92-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="90f92-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-InstrumentationKey <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90f92-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90f92-107">DESCRIPTION</span></span>
<span data-ttu-id="90f92-108">Cmdleten **set-AzureRmApiManagementLogger** ändrar inställningar för en Azure API Management- **loggning**.</span><span class="sxs-lookup"><span data-stu-id="90f92-108">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="90f92-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90f92-109">EXAMPLES</span></span>

### <span data-ttu-id="90f92-110">Exempel 1: ändra EventHub-loggning</span><span class="sxs-lookup"><span data-stu-id="90f92-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="90f92-111">Det här kommandot ändrar en loggare som har ID-Logger123.</span><span class="sxs-lookup"><span data-stu-id="90f92-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="90f92-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90f92-112">PARAMETERS</span></span>

### <span data-ttu-id="90f92-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="90f92-113">-ConnectionString</span></span>
<span data-ttu-id="90f92-114">Anger en anslutnings sträng för Azure Event Hubs som innehåller rättigheter för att skicka principer.</span><span class="sxs-lookup"><span data-stu-id="90f92-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="90f92-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="90f92-115">-Context</span></span>
<span data-ttu-id="90f92-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="90f92-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="90f92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90f92-117">-DefaultProfile</span></span>
<span data-ttu-id="90f92-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90f92-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90f92-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="90f92-119">-Description</span></span>
<span data-ttu-id="90f92-120">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="90f92-120">Specifies a description.</span></span>

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

### <span data-ttu-id="90f92-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="90f92-121">-InstrumentationKey</span></span>
<span data-ttu-id="90f92-122">Instrumentation-tangenten för program insikter.</span><span class="sxs-lookup"><span data-stu-id="90f92-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="90f92-123">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="90f92-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="90f92-124">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="90f92-124">-IsBuffered</span></span>
<span data-ttu-id="90f92-125">Anger att posterna i logg filen buffras innan de publiceras.</span><span class="sxs-lookup"><span data-stu-id="90f92-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="90f92-126">När posterna buffras skickas de till händelse NAV var 15: e sekund, eller när bufferten tar emot 256 KB av meddelanden.</span><span class="sxs-lookup"><span data-stu-id="90f92-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="90f92-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="90f92-127">-LoggerId</span></span>
<span data-ttu-id="90f92-128">Anger ID för den loggade loggningen.</span><span class="sxs-lookup"><span data-stu-id="90f92-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="90f92-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="90f92-129">-Name</span></span>
<span data-ttu-id="90f92-130">Anger entitetsnamnet för en händelsehubben från Azure Classic-portalen.</span><span class="sxs-lookup"><span data-stu-id="90f92-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="90f92-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90f92-131">-PassThru</span></span>
<span data-ttu-id="90f92-132">Anger att denna cmdlet returnerar  **PsApiManagementLogger** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="90f92-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="90f92-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90f92-133">CommonParameters</span></span>
<span data-ttu-id="90f92-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90f92-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90f92-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90f92-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90f92-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90f92-136">INPUTS</span></span>

### <span data-ttu-id="90f92-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="90f92-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="90f92-138">System. String</span><span class="sxs-lookup"><span data-stu-id="90f92-138">System.String</span></span>

### <span data-ttu-id="90f92-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="90f92-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="90f92-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90f92-140">OUTPUTS</span></span>

### <span data-ttu-id="90f92-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="90f92-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="90f92-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90f92-142">NOTES</span></span>

## <span data-ttu-id="90f92-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90f92-143">RELATED LINKS</span></span>

[<span data-ttu-id="90f92-144">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="90f92-144">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="90f92-145">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="90f92-145">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="90f92-146">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="90f92-146">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


