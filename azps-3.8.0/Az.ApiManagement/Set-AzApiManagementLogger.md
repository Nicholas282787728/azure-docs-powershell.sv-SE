---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 6ad32b3bd9bef4f4e684125b280db941da7a7b3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091906"
---
# <span data-ttu-id="3b3fc-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3b3fc-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="3b3fc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b3fc-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3fc-103">Ändrar en API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="3b3fc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b3fc-104">SYNTAX</span></span>

### <span data-ttu-id="3b3fc-105">EventHubLoggerSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3b3fc-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b3fc-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="3b3fc-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b3fc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b3fc-107">DESCRIPTION</span></span>
<span data-ttu-id="3b3fc-108">Cmdleten **set-AzApiManagementLogger** ändrar inställningar för en Azure API Management- **loggning**.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="3b3fc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b3fc-109">EXAMPLES</span></span>

### <span data-ttu-id="3b3fc-110">Exempel 1: ändra EventHub-loggning</span><span class="sxs-lookup"><span data-stu-id="3b3fc-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="3b3fc-111">Det här kommandot ändrar en loggare som har ID-Logger123.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="3b3fc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b3fc-112">PARAMETERS</span></span>

### <span data-ttu-id="3b3fc-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="3b3fc-113">-ConnectionString</span></span>
<span data-ttu-id="3b3fc-114">Anger en anslutnings sträng för Azure Event Hubs som innehåller rättigheter för att skicka principer.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="3b3fc-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3b3fc-115">-Context</span></span>
<span data-ttu-id="3b3fc-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3b3fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3fc-117">-DefaultProfile</span></span>
<span data-ttu-id="3b3fc-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b3fc-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3b3fc-119">-Description</span></span>
<span data-ttu-id="3b3fc-120">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-120">Specifies a description.</span></span>

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

### <span data-ttu-id="3b3fc-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="3b3fc-121">-InstrumentationKey</span></span>
<span data-ttu-id="3b3fc-122">Instrumentation-tangenten för program insikter.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="3b3fc-123">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="3b3fc-124">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="3b3fc-124">-IsBuffered</span></span>
<span data-ttu-id="3b3fc-125">Anger att posterna i logg filen buffras innan de publiceras.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="3b3fc-126">När posterna buffras skickas de till händelse NAV var 15: e sekund, eller när bufferten tar emot 256 KB av meddelanden.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="3b3fc-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="3b3fc-127">-LoggerId</span></span>
<span data-ttu-id="3b3fc-128">Anger ID för den loggade loggningen.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="3b3fc-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="3b3fc-129">-Name</span></span>
<span data-ttu-id="3b3fc-130">Anger entitetsnamnet för en händelsehubben från Azure Classic-portalen.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="3b3fc-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b3fc-131">-PassThru</span></span>
<span data-ttu-id="3b3fc-132">Anger att denna cmdlet returnerar  **PsApiManagementLogger** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3b3fc-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3b3fc-133">-Confirm</span></span>
<span data-ttu-id="3b3fc-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3fc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b3fc-135">-WhatIf</span></span>
<span data-ttu-id="3b3fc-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b3fc-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3fc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3fc-138">CommonParameters</span></span>
<span data-ttu-id="3b3fc-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b3fc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3fc-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b3fc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3fc-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b3fc-141">INPUTS</span></span>

### <span data-ttu-id="3b3fc-142">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3b3fc-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3b3fc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="3b3fc-143">System.String</span></span>

### <span data-ttu-id="3b3fc-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3b3fc-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3b3fc-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b3fc-145">OUTPUTS</span></span>

### <span data-ttu-id="3b3fc-146">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3b3fc-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="3b3fc-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b3fc-147">NOTES</span></span>

## <span data-ttu-id="3b3fc-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b3fc-148">RELATED LINKS</span></span>

[<span data-ttu-id="3b3fc-149">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3b3fc-149">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="3b3fc-150">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3b3fc-150">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="3b3fc-151">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3b3fc-151">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)


