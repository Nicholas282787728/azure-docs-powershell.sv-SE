---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 99c5cef4a15619da455b3e7ba1c7891652b991f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583871"
---
# <span data-ttu-id="2fbf9-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2fbf9-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="2fbf9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2fbf9-102">SYNOPSIS</span></span>
<span data-ttu-id="2fbf9-103">Konfigurerar en API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="2fbf9-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fbf9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2fbf9-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fbf9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2fbf9-105">DESCRIPTION</span></span>
<span data-ttu-id="2fbf9-106">Cmdleten **set-AzureRmApiManagementGroup** konfigurerar en API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="2fbf9-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="2fbf9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2fbf9-107">EXAMPLES</span></span>

### <span data-ttu-id="2fbf9-108">Exempel 1: Konfigurera en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="2fbf9-108">Example 1: Configure a management group</span></span>
```
PS C:\>Set-AzureRmApiManagementGroup -Context $APImContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="2fbf9-109">Det här kommandot konfigurerar en hanterings grupp som heter Group0001.</span><span class="sxs-lookup"><span data-stu-id="2fbf9-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="2fbf9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2fbf9-110">PARAMETERS</span></span>

### <span data-ttu-id="2fbf9-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2fbf9-111">-Context</span></span>
<span data-ttu-id="2fbf9-112">Anger en instans av ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2fbf9-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2fbf9-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="2fbf9-113">-Description</span></span>
<span data-ttu-id="2fbf9-114">Anger beskrivningen av hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="2fbf9-114">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="2fbf9-115">-Kund-</span><span class="sxs-lookup"><span data-stu-id="2fbf9-115">-GroupId</span></span>
<span data-ttu-id="2fbf9-116">Anger ID för hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="2fbf9-116">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="2fbf9-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2fbf9-117">-Name</span></span>
<span data-ttu-id="2fbf9-118">Anger namnet på hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="2fbf9-118">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="2fbf9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fbf9-119">-PassThru</span></span>
<span data-ttu-id="2fbf9-120">passthru</span><span class="sxs-lookup"><span data-stu-id="2fbf9-120">passthru</span></span>

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

### <span data-ttu-id="2fbf9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fbf9-121">-DefaultProfile</span></span>
<span data-ttu-id="2fbf9-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2fbf9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fbf9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fbf9-123">CommonParameters</span></span>
<span data-ttu-id="2fbf9-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fbf9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fbf9-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fbf9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fbf9-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2fbf9-126">INPUTS</span></span>

## <span data-ttu-id="2fbf9-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2fbf9-127">OUTPUTS</span></span>

### <span data-ttu-id="2fbf9-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2fbf9-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="2fbf9-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2fbf9-129">NOTES</span></span>

## <span data-ttu-id="2fbf9-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2fbf9-130">RELATED LINKS</span></span>

[<span data-ttu-id="2fbf9-131">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2fbf9-131">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="2fbf9-132">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2fbf9-132">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="2fbf9-133">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2fbf9-133">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


