---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: a60f39f6abf81af00e617c454c3af2f8bb682749
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756739"
---
# <span data-ttu-id="b0e37-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b0e37-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="b0e37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0e37-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e37-103">Tar bort en API-egenskap.</span><span class="sxs-lookup"><span data-stu-id="b0e37-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0e37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0e37-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0e37-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0e37-105">DESCRIPTION</span></span>
<span data-ttu-id="b0e37-106">Cmdleten **Remove-AzureRmApiManagementProperty** tar bort en Azure API Management- **egenskap**.</span><span class="sxs-lookup"><span data-stu-id="b0e37-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="b0e37-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0e37-107">EXAMPLES</span></span>

### <span data-ttu-id="b0e37-108">Exempel 1: ta bort en egenskap</span><span class="sxs-lookup"><span data-stu-id="b0e37-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="b0e37-109">Det här kommandot tar bort egenskapen med ID-Property11.</span><span class="sxs-lookup"><span data-stu-id="b0e37-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="b0e37-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0e37-110">PARAMETERS</span></span>

### <span data-ttu-id="b0e37-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b0e37-111">-Context</span></span>
<span data-ttu-id="b0e37-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b0e37-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b0e37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e37-113">-DefaultProfile</span></span>
<span data-ttu-id="b0e37-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0e37-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0e37-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0e37-115">-PassThru</span></span>
<span data-ttu-id="b0e37-116">Anger att denna cmdlet returnerar ett värde för $True om åtgärden lyckas eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="b0e37-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="b0e37-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="b0e37-117">-PropertyId</span></span>
<span data-ttu-id="b0e37-118">Anger ett ID för den egenskap som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="b0e37-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b0e37-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b0e37-119">-Confirm</span></span>
<span data-ttu-id="b0e37-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b0e37-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0e37-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0e37-121">-WhatIf</span></span>
<span data-ttu-id="b0e37-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b0e37-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0e37-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b0e37-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0e37-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e37-124">CommonParameters</span></span>
<span data-ttu-id="b0e37-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0e37-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e37-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0e37-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e37-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0e37-127">INPUTS</span></span>

### <span data-ttu-id="b0e37-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b0e37-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b0e37-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b0e37-129">System.String</span></span>

### <span data-ttu-id="b0e37-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b0e37-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b0e37-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0e37-131">OUTPUTS</span></span>

### <span data-ttu-id="b0e37-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0e37-132">System.Boolean</span></span>

## <span data-ttu-id="b0e37-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0e37-133">NOTES</span></span>

## <span data-ttu-id="b0e37-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0e37-134">RELATED LINKS</span></span>

[<span data-ttu-id="b0e37-135">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b0e37-135">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="b0e37-136">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="b0e37-136">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


