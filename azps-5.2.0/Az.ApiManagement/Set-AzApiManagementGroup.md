---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: f4e2bb2bce0dc01f99b55497ba671999c9c2ab01
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414080"
---
# <span data-ttu-id="61767-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="61767-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="61767-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61767-102">SYNOPSIS</span></span>
<span data-ttu-id="61767-103">Konfigurerar en API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="61767-103">Configures an API management group.</span></span>

## <span data-ttu-id="61767-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61767-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61767-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61767-105">DESCRIPTION</span></span>
<span data-ttu-id="61767-106">Cmdleten **set-AzApiManagementGroup** konfigurerar en API-hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="61767-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="61767-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61767-107">EXAMPLES</span></span>

### <span data-ttu-id="61767-108">Exempel 1: Konfigurera en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="61767-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="61767-109">Det här kommandot konfigurerar en hanterings grupp som heter Group0001.</span><span class="sxs-lookup"><span data-stu-id="61767-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="61767-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61767-110">PARAMETERS</span></span>

### <span data-ttu-id="61767-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="61767-111">-Context</span></span>
<span data-ttu-id="61767-112">Anger en instans av ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="61767-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="61767-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61767-113">-DefaultProfile</span></span>
<span data-ttu-id="61767-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="61767-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61767-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="61767-115">-Description</span></span>
<span data-ttu-id="61767-116">Anger beskrivningen av hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="61767-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="61767-117">-Kund-</span><span class="sxs-lookup"><span data-stu-id="61767-117">-GroupId</span></span>
<span data-ttu-id="61767-118">Anger ID för hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="61767-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="61767-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="61767-119">-Name</span></span>
<span data-ttu-id="61767-120">Anger namnet på hanterings gruppen.</span><span class="sxs-lookup"><span data-stu-id="61767-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="61767-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61767-121">-PassThru</span></span>
<span data-ttu-id="61767-122">passthru</span><span class="sxs-lookup"><span data-stu-id="61767-122">passthru</span></span>

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

### <span data-ttu-id="61767-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="61767-123">-Confirm</span></span>
<span data-ttu-id="61767-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="61767-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61767-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61767-125">-WhatIf</span></span>
<span data-ttu-id="61767-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="61767-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61767-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="61767-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61767-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61767-128">CommonParameters</span></span>
<span data-ttu-id="61767-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61767-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61767-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61767-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61767-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61767-131">INPUTS</span></span>

### <span data-ttu-id="61767-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="61767-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="61767-133">System. String</span><span class="sxs-lookup"><span data-stu-id="61767-133">System.String</span></span>

### <span data-ttu-id="61767-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="61767-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="61767-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61767-135">OUTPUTS</span></span>

### <span data-ttu-id="61767-136">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="61767-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="61767-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61767-137">NOTES</span></span>

## <span data-ttu-id="61767-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61767-138">RELATED LINKS</span></span>

[<span data-ttu-id="61767-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="61767-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="61767-140">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="61767-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="61767-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="61767-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


