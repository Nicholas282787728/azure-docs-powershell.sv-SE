---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 058a82398be387913a0dd3eaf58c80ac12b692dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574079"
---
# <span data-ttu-id="68cf3-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="68cf3-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="68cf3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="68cf3-103">Konfigurerar en API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="68cf3-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68cf3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68cf3-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68cf3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68cf3-105">DESCRIPTION</span></span>
<span data-ttu-id="68cf3-106">Cmdleten **set-AzureRmApiManagementGroup** konfigurerar en API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="68cf3-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="68cf3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68cf3-107">EXAMPLES</span></span>

### <span data-ttu-id="68cf3-108">Exempel 1: Konfigurera en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="68cf3-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="68cf3-109">Det här kommandot konfigurerar en hanterings grupp som heter Group0001.</span><span class="sxs-lookup"><span data-stu-id="68cf3-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="68cf3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68cf3-110">PARAMETERS</span></span>

### <span data-ttu-id="68cf3-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="68cf3-111">-Context</span></span>
<span data-ttu-id="68cf3-112">Anger en instans av ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="68cf3-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="68cf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68cf3-113">-DefaultProfile</span></span>
<span data-ttu-id="68cf3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="68cf3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68cf3-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="68cf3-115">-Description</span></span>
<span data-ttu-id="68cf3-116">Anger beskrivningen av hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="68cf3-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="68cf3-117">-Kund-</span><span class="sxs-lookup"><span data-stu-id="68cf3-117">-GroupId</span></span>
<span data-ttu-id="68cf3-118">Anger ID för hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="68cf3-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="68cf3-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="68cf3-119">-Name</span></span>
<span data-ttu-id="68cf3-120">Anger namnet på hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="68cf3-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="68cf3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68cf3-121">-PassThru</span></span>
<span data-ttu-id="68cf3-122">passthru</span><span class="sxs-lookup"><span data-stu-id="68cf3-122">passthru</span></span>

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

### <span data-ttu-id="68cf3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68cf3-123">CommonParameters</span></span>
<span data-ttu-id="68cf3-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68cf3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68cf3-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68cf3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68cf3-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68cf3-126">INPUTS</span></span>

### <span data-ttu-id="68cf3-127">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="68cf3-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="68cf3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="68cf3-128">System.String</span></span>

### <span data-ttu-id="68cf3-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="68cf3-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="68cf3-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68cf3-130">OUTPUTS</span></span>

### <span data-ttu-id="68cf3-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="68cf3-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="68cf3-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68cf3-132">NOTES</span></span>

## <span data-ttu-id="68cf3-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68cf3-133">RELATED LINKS</span></span>

[<span data-ttu-id="68cf3-134">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="68cf3-134">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="68cf3-135">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="68cf3-135">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="68cf3-136">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="68cf3-136">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


