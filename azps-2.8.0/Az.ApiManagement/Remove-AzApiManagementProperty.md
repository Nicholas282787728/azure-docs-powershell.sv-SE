---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
ms.openlocfilehash: 323cbbdc38281c9b90ab3728eb2879bf1b7bfe89
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745695"
---
# <span data-ttu-id="95611-101">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="95611-101">Remove-AzApiManagementProperty</span></span>

## <span data-ttu-id="95611-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95611-102">SYNOPSIS</span></span>
<span data-ttu-id="95611-103">Tar bort en API-egenskap.</span><span class="sxs-lookup"><span data-stu-id="95611-103">Removes an API Management Property.</span></span>

## <span data-ttu-id="95611-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95611-104">SYNTAX</span></span>

```
Remove-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95611-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95611-105">DESCRIPTION</span></span>
<span data-ttu-id="95611-106">Cmdleten **Remove-AzApiManagementProperty** tar bort en Azure API Management- **egenskap**.</span><span class="sxs-lookup"><span data-stu-id="95611-106">The **Remove-AzApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="95611-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95611-107">EXAMPLES</span></span>

### <span data-ttu-id="95611-108">Exempel 1: ta bort en egenskap</span><span class="sxs-lookup"><span data-stu-id="95611-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="95611-109">Det här kommandot tar bort egenskapen med ID-Property11.</span><span class="sxs-lookup"><span data-stu-id="95611-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="95611-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95611-110">PARAMETERS</span></span>

### <span data-ttu-id="95611-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="95611-111">-Context</span></span>
<span data-ttu-id="95611-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="95611-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="95611-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95611-113">-DefaultProfile</span></span>
<span data-ttu-id="95611-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95611-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95611-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95611-115">-PassThru</span></span>
<span data-ttu-id="95611-116">Anger att denna cmdlet returnerar ett värde för $True om åtgärden lyckas eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="95611-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="95611-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="95611-117">-PropertyId</span></span>
<span data-ttu-id="95611-118">Anger ett ID för den egenskap som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="95611-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="95611-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="95611-119">-Confirm</span></span>
<span data-ttu-id="95611-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="95611-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95611-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95611-121">-WhatIf</span></span>
<span data-ttu-id="95611-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="95611-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95611-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="95611-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95611-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95611-124">CommonParameters</span></span>
<span data-ttu-id="95611-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95611-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95611-126">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95611-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95611-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95611-127">INPUTS</span></span>

### <span data-ttu-id="95611-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="95611-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="95611-129">System. String</span><span class="sxs-lookup"><span data-stu-id="95611-129">System.String</span></span>

### <span data-ttu-id="95611-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="95611-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="95611-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95611-131">OUTPUTS</span></span>

### <span data-ttu-id="95611-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95611-132">System.Boolean</span></span>

## <span data-ttu-id="95611-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95611-133">NOTES</span></span>

## <span data-ttu-id="95611-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95611-134">RELATED LINKS</span></span>

[<span data-ttu-id="95611-135">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="95611-135">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="95611-136">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="95611-136">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


