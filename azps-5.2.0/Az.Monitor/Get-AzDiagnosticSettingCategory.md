---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: 2d1c4b2f272516af31fba17db50d33991dd1db50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415152"
---
# <span data-ttu-id="9516f-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="9516f-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="9516f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9516f-102">SYNOPSIS</span></span>
<span data-ttu-id="9516f-103">Lista med diagnostisk inställning som stöds av Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="9516f-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="9516f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9516f-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9516f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9516f-105">DESCRIPTION</span></span>
<span data-ttu-id="9516f-106">Lista med diagnostisk inställning som stöds av Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="9516f-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="9516f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9516f-107">EXAMPLES</span></span>

### <span data-ttu-id="9516f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9516f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSetting -TargetResourceId -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="9516f-109">Tillgängliga diagnostiska inställnings kategorier för virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="9516f-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="9516f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9516f-110">PARAMETERS</span></span>

### <span data-ttu-id="9516f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9516f-111">-DefaultProfile</span></span>
<span data-ttu-id="9516f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9516f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9516f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9516f-113">-Name</span></span>
<span data-ttu-id="9516f-114">Namn på kategorin diagnostisk inställning</span><span class="sxs-lookup"><span data-stu-id="9516f-114">Name of diagnostic setting category</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9516f-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9516f-115">-TargetResourceId</span></span>
<span data-ttu-id="9516f-116">Mål resurs-ID</span><span class="sxs-lookup"><span data-stu-id="9516f-116">Target resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9516f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9516f-117">CommonParameters</span></span>
<span data-ttu-id="9516f-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9516f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9516f-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9516f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9516f-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9516f-120">INPUTS</span></span>

### <span data-ttu-id="9516f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9516f-121">System.String</span></span>

## <span data-ttu-id="9516f-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9516f-122">OUTPUTS</span></span>

### <span data-ttu-id="9516f-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="9516f-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="9516f-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9516f-124">NOTES</span></span>

## <span data-ttu-id="9516f-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9516f-125">RELATED LINKS</span></span>
