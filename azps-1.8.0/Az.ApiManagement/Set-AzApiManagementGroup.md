---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: 027e07ed495cb5b80fbd05852b640526c87bf16e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917693"
---
# <span data-ttu-id="0352a-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0352a-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="0352a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0352a-102">SYNOPSIS</span></span>
<span data-ttu-id="0352a-103">Konfigurerar en API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="0352a-103">Configures an API management group.</span></span>

## <span data-ttu-id="0352a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0352a-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0352a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0352a-105">DESCRIPTION</span></span>
<span data-ttu-id="0352a-106">Cmdleten **set-AzApiManagementGroup** konfigurerar en API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="0352a-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="0352a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0352a-107">EXAMPLES</span></span>

### <span data-ttu-id="0352a-108">Exempel 1: Konfigurera en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="0352a-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="0352a-109">Det här kommandot konfigurerar en hanterings grupp som heter Group0001.</span><span class="sxs-lookup"><span data-stu-id="0352a-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="0352a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0352a-110">PARAMETERS</span></span>

### <span data-ttu-id="0352a-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="0352a-111">-Context</span></span>
<span data-ttu-id="0352a-112">Anger en instans av ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0352a-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0352a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0352a-113">-DefaultProfile</span></span>
<span data-ttu-id="0352a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0352a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0352a-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="0352a-115">-Description</span></span>
<span data-ttu-id="0352a-116">Anger beskrivningen av hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="0352a-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="0352a-117">-Kund-</span><span class="sxs-lookup"><span data-stu-id="0352a-117">-GroupId</span></span>
<span data-ttu-id="0352a-118">Anger ID för hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="0352a-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="0352a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="0352a-119">-Name</span></span>
<span data-ttu-id="0352a-120">Anger namnet på hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="0352a-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="0352a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0352a-121">-PassThru</span></span>
<span data-ttu-id="0352a-122">passthru</span><span class="sxs-lookup"><span data-stu-id="0352a-122">passthru</span></span>

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

### <span data-ttu-id="0352a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0352a-123">CommonParameters</span></span>
<span data-ttu-id="0352a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0352a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0352a-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0352a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0352a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0352a-126">INPUTS</span></span>

### <span data-ttu-id="0352a-127">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0352a-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0352a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0352a-128">System.String</span></span>

### <span data-ttu-id="0352a-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0352a-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0352a-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0352a-130">OUTPUTS</span></span>

### <span data-ttu-id="0352a-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0352a-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="0352a-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0352a-132">NOTES</span></span>

## <span data-ttu-id="0352a-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0352a-133">RELATED LINKS</span></span>

[<span data-ttu-id="0352a-134">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0352a-134">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="0352a-135">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0352a-135">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="0352a-136">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0352a-136">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


