---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 16a60f5f9951aaa40ac8da8584e1c2690206cdb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585204"
---
# <span data-ttu-id="41c07-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="41c07-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="41c07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41c07-102">SYNOPSIS</span></span>
<span data-ttu-id="41c07-103">Ändrar en API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="41c07-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41c07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41c07-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41c07-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41c07-105">DESCRIPTION</span></span>
<span data-ttu-id="41c07-106">Cmdleten **set-AzureRmApiManagementLogger** ändrar inställningar för en Azure API Management- **loggning**.</span><span class="sxs-lookup"><span data-stu-id="41c07-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="41c07-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41c07-107">EXAMPLES</span></span>

### <span data-ttu-id="41c07-108">Exempel 1: ändra en loggare</span><span class="sxs-lookup"><span data-stu-id="41c07-108">Example 1: Modify a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="41c07-109">Det här kommandot ändrar en loggare som har ID-Logger123.</span><span class="sxs-lookup"><span data-stu-id="41c07-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="41c07-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41c07-110">PARAMETERS</span></span>

### <span data-ttu-id="41c07-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="41c07-111">-ConnectionString</span></span>
<span data-ttu-id="41c07-112">Anger en anslutnings sträng för Azure Event Hubs som innehåller rättigheter för att skicka principer.</span><span class="sxs-lookup"><span data-stu-id="41c07-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="41c07-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="41c07-113">-Context</span></span>
<span data-ttu-id="41c07-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="41c07-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="41c07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c07-115">-DefaultProfile</span></span>
<span data-ttu-id="41c07-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="41c07-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="41c07-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="41c07-117">-Description</span></span>
<span data-ttu-id="41c07-118">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="41c07-118">Specifies a description.</span></span>

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

### <span data-ttu-id="41c07-119">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="41c07-119">-IsBuffered</span></span>
<span data-ttu-id="41c07-120">Anger att posterna i logg filen buffras innan de publiceras.</span><span class="sxs-lookup"><span data-stu-id="41c07-120">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="41c07-121">När posterna buffras skickas de till händelse NAV var 15: e sekund, eller när bufferten tar emot 256 KB av meddelanden.</span><span class="sxs-lookup"><span data-stu-id="41c07-121">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c07-122">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="41c07-122">-LoggerId</span></span>
<span data-ttu-id="41c07-123">Anger ID för den loggade loggningen.</span><span class="sxs-lookup"><span data-stu-id="41c07-123">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="41c07-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="41c07-124">-Name</span></span>
<span data-ttu-id="41c07-125">Anger entitetsnamnet för en händelsehubben från Azure Classic-portalen.</span><span class="sxs-lookup"><span data-stu-id="41c07-125">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="41c07-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41c07-126">-PassThru</span></span>
<span data-ttu-id="41c07-127">Anger att denna cmdlet returnerar  **PsApiManagementLogger** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="41c07-127">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c07-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c07-128">CommonParameters</span></span>
<span data-ttu-id="41c07-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41c07-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c07-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41c07-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c07-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41c07-131">INPUTS</span></span>

### <span data-ttu-id="41c07-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="41c07-132">None</span></span>
<span data-ttu-id="41c07-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="41c07-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="41c07-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41c07-134">OUTPUTS</span></span>

### <span data-ttu-id="41c07-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="41c07-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="41c07-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41c07-136">NOTES</span></span>

## <span data-ttu-id="41c07-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41c07-137">RELATED LINKS</span></span>

[<span data-ttu-id="41c07-138">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="41c07-138">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="41c07-139">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="41c07-139">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="41c07-140">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="41c07-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


