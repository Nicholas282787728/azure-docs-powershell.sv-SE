---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394120"
---
# <span data-ttu-id="a8cdd-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8cdd-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="a8cdd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="a8cdd-103">Hämta underhålls konfigurations post</span><span class="sxs-lookup"><span data-stu-id="a8cdd-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="a8cdd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8cdd-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8cdd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8cdd-105">DESCRIPTION</span></span>
<span data-ttu-id="a8cdd-106">Hämta underhålls konfigurations post</span><span class="sxs-lookup"><span data-stu-id="a8cdd-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="a8cdd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8cdd-107">EXAMPLES</span></span>

### <span data-ttu-id="a8cdd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a8cdd-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="a8cdd-109">Hämta underhålls konfigurations post</span><span class="sxs-lookup"><span data-stu-id="a8cdd-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="a8cdd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8cdd-110">PARAMETERS</span></span>

### <span data-ttu-id="a8cdd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8cdd-111">-DefaultProfile</span></span>
<span data-ttu-id="a8cdd-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8cdd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8cdd-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8cdd-113">-Name</span></span>
<span data-ttu-id="a8cdd-114">Konfigurations namn för underhåll.</span><span class="sxs-lookup"><span data-stu-id="a8cdd-114">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8cdd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8cdd-115">-ResourceGroupName</span></span>
<span data-ttu-id="a8cdd-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a8cdd-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8cdd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8cdd-117">CommonParameters</span></span>
<span data-ttu-id="a8cdd-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8cdd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8cdd-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8cdd-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8cdd-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8cdd-120">INPUTS</span></span>

### <span data-ttu-id="a8cdd-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a8cdd-121">System.String</span></span>

## <span data-ttu-id="a8cdd-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8cdd-122">OUTPUTS</span></span>

### <span data-ttu-id="a8cdd-123">Microsoft. Azure. commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8cdd-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="a8cdd-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8cdd-124">NOTES</span></span>

## <span data-ttu-id="a8cdd-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8cdd-125">RELATED LINKS</span></span>
