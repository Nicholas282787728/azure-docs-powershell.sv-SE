---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 2dbd515877e44023077d782080cff29d78a0e6fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585207"
---
# <span data-ttu-id="eff5f-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="eff5f-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="eff5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eff5f-102">SYNOPSIS</span></span>
<span data-ttu-id="eff5f-103">Tar bort en API-hanteringskonsolen.</span><span class="sxs-lookup"><span data-stu-id="eff5f-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eff5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eff5f-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eff5f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eff5f-105">DESCRIPTION</span></span>
<span data-ttu-id="eff5f-106">Cmdleten **Remove-AzureRmApiManagementLogger** tar bort en Azure API Management- **loggning**.</span><span class="sxs-lookup"><span data-stu-id="eff5f-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="eff5f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eff5f-107">EXAMPLES</span></span>

### <span data-ttu-id="eff5f-108">Exempel 1: ta bort en loggare</span><span class="sxs-lookup"><span data-stu-id="eff5f-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="eff5f-109">Det här kommandot tar bort en loggare som har ID-Logger123.</span><span class="sxs-lookup"><span data-stu-id="eff5f-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="eff5f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eff5f-110">PARAMETERS</span></span>

### <span data-ttu-id="eff5f-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="eff5f-111">-Context</span></span>
<span data-ttu-id="eff5f-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="eff5f-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="eff5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff5f-113">-DefaultProfile</span></span>
<span data-ttu-id="eff5f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eff5f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="eff5f-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="eff5f-115">-LoggerId</span></span>
<span data-ttu-id="eff5f-116">Anger ID för den logg som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="eff5f-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="eff5f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eff5f-117">-PassThru</span></span>
<span data-ttu-id="eff5f-118">Anger att denna cmdlet returnerar ett värde för $True om åtgärden lyckas eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="eff5f-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="eff5f-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eff5f-119">-Confirm</span></span>
<span data-ttu-id="eff5f-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eff5f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eff5f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eff5f-121">-WhatIf</span></span>
<span data-ttu-id="eff5f-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eff5f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eff5f-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eff5f-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eff5f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff5f-124">CommonParameters</span></span>
<span data-ttu-id="eff5f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eff5f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff5f-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eff5f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff5f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eff5f-127">INPUTS</span></span>

### <span data-ttu-id="eff5f-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="eff5f-128">None</span></span>
<span data-ttu-id="eff5f-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="eff5f-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eff5f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eff5f-130">OUTPUTS</span></span>

### <span data-ttu-id="eff5f-131">Returtyp</span><span class="sxs-lookup"><span data-stu-id="eff5f-131">Boolean</span></span>

## <span data-ttu-id="eff5f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eff5f-132">NOTES</span></span>

## <span data-ttu-id="eff5f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eff5f-133">RELATED LINKS</span></span>

[<span data-ttu-id="eff5f-134">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="eff5f-134">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="eff5f-135">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="eff5f-135">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="eff5f-136">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="eff5f-136">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


