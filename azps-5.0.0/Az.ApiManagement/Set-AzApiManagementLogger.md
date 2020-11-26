---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 1c32681425136261ca54ed6dac1501d885318df1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269372"
---
# <span data-ttu-id="46e6d-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="46e6d-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="46e6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="46e6d-103">Ändrar en API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="46e6d-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="46e6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46e6d-104">SYNTAX</span></span>

### <span data-ttu-id="46e6d-105">EventHubLoggerSet (standard)</span><span class="sxs-lookup"><span data-stu-id="46e6d-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46e6d-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="46e6d-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46e6d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46e6d-107">DESCRIPTION</span></span>
<span data-ttu-id="46e6d-108">Cmdleten **set-AzApiManagementLogger** ändrar inställningar för en Azure API Management- **loggning**.</span><span class="sxs-lookup"><span data-stu-id="46e6d-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="46e6d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46e6d-109">EXAMPLES</span></span>

### <span data-ttu-id="46e6d-110">Exempel 1: ändra EventHub-loggning</span><span class="sxs-lookup"><span data-stu-id="46e6d-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="46e6d-111">Det här kommandot ändrar en loggare som har ID-Logger123.</span><span class="sxs-lookup"><span data-stu-id="46e6d-111">This command modifies a logger that has the ID Logger123.</span></span>

### <span data-ttu-id="46e6d-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="46e6d-112">Example 2</span></span>

<span data-ttu-id="46e6d-113">Ändrar en API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="46e6d-113">Modifies an API Management Logger.</span></span> <span data-ttu-id="46e6d-114">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="46e6d-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementLogger -Confirm -Context <PsApiManagementContext> -InstrumentationKey <String> -LoggerId 'Logger123'
```

## <span data-ttu-id="46e6d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46e6d-115">PARAMETERS</span></span>

### <span data-ttu-id="46e6d-116">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="46e6d-116">-ConnectionString</span></span>
<span data-ttu-id="46e6d-117">Anger en anslutnings sträng för Azure Event Hubs som innehåller rättigheter för att skicka principer.</span><span class="sxs-lookup"><span data-stu-id="46e6d-117">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="46e6d-118">-Kontext</span><span class="sxs-lookup"><span data-stu-id="46e6d-118">-Context</span></span>
<span data-ttu-id="46e6d-119">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="46e6d-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="46e6d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e6d-120">-DefaultProfile</span></span>
<span data-ttu-id="46e6d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46e6d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46e6d-122">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="46e6d-122">-Description</span></span>
<span data-ttu-id="46e6d-123">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="46e6d-123">Specifies a description.</span></span>

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

### <span data-ttu-id="46e6d-124">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="46e6d-124">-InstrumentationKey</span></span>
<span data-ttu-id="46e6d-125">Instrumentation-tangenten för program insikter.</span><span class="sxs-lookup"><span data-stu-id="46e6d-125">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="46e6d-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="46e6d-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="46e6d-127">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="46e6d-127">-IsBuffered</span></span>
<span data-ttu-id="46e6d-128">Anger att posterna i logg filen buffras innan de publiceras.</span><span class="sxs-lookup"><span data-stu-id="46e6d-128">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="46e6d-129">När posterna buffras skickas de till händelse NAV var 15: e sekund, eller när bufferten tar emot 256 KB av meddelanden.</span><span class="sxs-lookup"><span data-stu-id="46e6d-129">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="46e6d-130">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="46e6d-130">-LoggerId</span></span>
<span data-ttu-id="46e6d-131">Anger ID för den loggade loggningen.</span><span class="sxs-lookup"><span data-stu-id="46e6d-131">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="46e6d-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="46e6d-132">-Name</span></span>
<span data-ttu-id="46e6d-133">Anger entitetsnamnet för en händelsehubben från Azure Classic-portalen.</span><span class="sxs-lookup"><span data-stu-id="46e6d-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="46e6d-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46e6d-134">-PassThru</span></span>
<span data-ttu-id="46e6d-135">Anger att denna cmdlet returnerar  **PsApiManagementLogger** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="46e6d-135">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="46e6d-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="46e6d-136">-Confirm</span></span>
<span data-ttu-id="46e6d-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="46e6d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46e6d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46e6d-138">-WhatIf</span></span>
<span data-ttu-id="46e6d-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="46e6d-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46e6d-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="46e6d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46e6d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e6d-141">CommonParameters</span></span>
<span data-ttu-id="46e6d-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46e6d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e6d-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46e6d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e6d-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46e6d-144">INPUTS</span></span>

### <span data-ttu-id="46e6d-145">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="46e6d-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="46e6d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="46e6d-146">System.String</span></span>

### <span data-ttu-id="46e6d-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="46e6d-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="46e6d-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46e6d-148">OUTPUTS</span></span>

### <span data-ttu-id="46e6d-149">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="46e6d-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="46e6d-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46e6d-150">NOTES</span></span>

## <span data-ttu-id="46e6d-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46e6d-151">RELATED LINKS</span></span>

[<span data-ttu-id="46e6d-152">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="46e6d-152">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="46e6d-153">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="46e6d-153">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="46e6d-154">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="46e6d-154">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

