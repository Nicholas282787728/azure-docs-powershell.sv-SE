---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 20f2f79c154cd16dcf09501bdbefb488fdeb61eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577277"
---
# <span data-ttu-id="78bff-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="78bff-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="78bff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78bff-102">SYNOPSIS</span></span>
<span data-ttu-id="78bff-103">Konfigurerar en API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="78bff-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78bff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78bff-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78bff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78bff-105">DESCRIPTION</span></span>
<span data-ttu-id="78bff-106">Cmdleten **set-AzureRmApiManagementGroup** konfigurerar en API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="78bff-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="78bff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78bff-107">EXAMPLES</span></span>

### <span data-ttu-id="78bff-108">Exempel 1: Konfigurera en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="78bff-108">Example 1: Configure a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="78bff-109">Det här kommandot konfigurerar en hanterings grupp som heter Group0001.</span><span class="sxs-lookup"><span data-stu-id="78bff-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="78bff-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78bff-110">PARAMETERS</span></span>

### <span data-ttu-id="78bff-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="78bff-111">-Context</span></span>
<span data-ttu-id="78bff-112">Anger en instans av ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="78bff-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="78bff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78bff-113">-DefaultProfile</span></span>
<span data-ttu-id="78bff-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="78bff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="78bff-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="78bff-115">-Description</span></span>
<span data-ttu-id="78bff-116">Anger beskrivningen av hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="78bff-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="78bff-117">-Kund-</span><span class="sxs-lookup"><span data-stu-id="78bff-117">-GroupId</span></span>
<span data-ttu-id="78bff-118">Anger ID för hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="78bff-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="78bff-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="78bff-119">-Name</span></span>
<span data-ttu-id="78bff-120">Anger namnet på hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="78bff-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="78bff-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78bff-121">-PassThru</span></span>
<span data-ttu-id="78bff-122">passthru</span><span class="sxs-lookup"><span data-stu-id="78bff-122">passthru</span></span>

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

### <span data-ttu-id="78bff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78bff-123">CommonParameters</span></span>
<span data-ttu-id="78bff-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78bff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78bff-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78bff-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78bff-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78bff-126">INPUTS</span></span>

### <span data-ttu-id="78bff-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="78bff-127">None</span></span>
<span data-ttu-id="78bff-128">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="78bff-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="78bff-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78bff-129">OUTPUTS</span></span>

### <span data-ttu-id="78bff-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="78bff-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="78bff-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78bff-131">NOTES</span></span>

## <span data-ttu-id="78bff-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78bff-132">RELATED LINKS</span></span>

[<span data-ttu-id="78bff-133">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="78bff-133">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="78bff-134">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="78bff-134">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="78bff-135">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="78bff-135">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


