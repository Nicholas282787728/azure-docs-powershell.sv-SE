---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 2f62b33b7a5a2224f54be765d03f72fc1667cec1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584255"
---
# <span data-ttu-id="5ac36-101">Remove-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="5ac36-101">Remove-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="5ac36-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ac36-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac36-103">Ta bort en diagnostisk inställning för en resurs.</span><span class="sxs-lookup"><span data-stu-id="5ac36-103">Remove a diagnostic setting for the a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ac36-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ac36-104">SYNTAX</span></span>

```
Remove-AzureRmDiagnosticSetting -ResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ac36-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ac36-105">DESCRIPTION</span></span>
<span data-ttu-id="5ac36-106">Cmdleten **Remove-AzureRmDiagnosticSetting** tar bort Diagnostikrapporten för den specifika resursen.</span><span class="sxs-lookup"><span data-stu-id="5ac36-106">The **Remove-AzureRmDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="5ac36-107">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="5ac36-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="5ac36-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ac36-108">EXAMPLES</span></span>

### <span data-ttu-id="5ac36-109">Exempel 1: ta bort standardinställningarna för diagnostik (tjänst) för en resurs</span><span class="sxs-lookup"><span data-stu-id="5ac36-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzureRmDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="5ac36-110">Det här kommandot tar bort standardinställningarna för diagnostik (tjänst) för resursen som heter Resource01.</span><span class="sxs-lookup"><span data-stu-id="5ac36-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="5ac36-111">Exempel 2: ta bort standardinställningen för diagnos som identifieras av det angivna namnet för en resurs</span><span class="sxs-lookup"><span data-stu-id="5ac36-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzureRmDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="5ac36-112">Det här kommandot tar bort Diagnostic-inställningen "myDiagSetting" för resursen som heter Resource01.</span><span class="sxs-lookup"><span data-stu-id="5ac36-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="5ac36-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ac36-113">PARAMETERS</span></span>

### <span data-ttu-id="5ac36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac36-114">-DefaultProfile</span></span>
<span data-ttu-id="5ac36-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ac36-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ac36-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ac36-116">-Name</span></span>
<span data-ttu-id="5ac36-117">Namnet på diagnos inställningen.</span><span class="sxs-lookup"><span data-stu-id="5ac36-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="5ac36-118">Om du inte har gett samtals standarden "tjänst" som att den fanns i föregående API och denna cmdlet inaktive ras bara alla kategorier för mått/loggar.</span><span class="sxs-lookup"><span data-stu-id="5ac36-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="5ac36-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ac36-119">-ResourceId</span></span>
<span data-ttu-id="5ac36-120">Anger ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="5ac36-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="5ac36-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ac36-121">-Confirm</span></span>
<span data-ttu-id="5ac36-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ac36-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ac36-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ac36-123">-WhatIf</span></span>
<span data-ttu-id="5ac36-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ac36-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ac36-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ac36-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ac36-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac36-126">CommonParameters</span></span>
<span data-ttu-id="5ac36-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac36-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac36-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ac36-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac36-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ac36-129">INPUTS</span></span>

### <span data-ttu-id="5ac36-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5ac36-130">System.String</span></span>

## <span data-ttu-id="5ac36-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ac36-131">OUTPUTS</span></span>

### <span data-ttu-id="5ac36-132">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5ac36-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="5ac36-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ac36-133">NOTES</span></span>

## <span data-ttu-id="5ac36-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ac36-134">RELATED LINKS</span></span>

<span data-ttu-id="5ac36-135">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md) 
 [Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="5ac36-135">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)
[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)</span></span>
