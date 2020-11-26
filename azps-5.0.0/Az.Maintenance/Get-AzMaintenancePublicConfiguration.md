---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenancepublicconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
ms.openlocfilehash: 8df9e8145e1acb03c0351f30565da2d9a8ed4a9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270584"
---
# <span data-ttu-id="f0788-101">Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0788-101">Get-AzMaintenancePublicConfiguration</span></span>

## <span data-ttu-id="f0788-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0788-102">SYNOPSIS</span></span>
<span data-ttu-id="f0788-103">Hämta konfigurations post för offentliga underhåll</span><span class="sxs-lookup"><span data-stu-id="f0788-103">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="f0788-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0788-104">SYNTAX</span></span>

```
Get-AzMaintenancePublicConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0788-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0788-105">DESCRIPTION</span></span>
<span data-ttu-id="f0788-106">Hämta konfigurations post för offentliga underhåll</span><span class="sxs-lookup"><span data-stu-id="f0788-106">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="f0788-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0788-107">EXAMPLES</span></span>

### <span data-ttu-id="f0788-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f0788-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenancePublicConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {"publicMaintenanceConfigurationId" : "workervmscentralus"}
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : SQLDB
Visibility          : Public
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/publicMaintenanceConfigurations
```

<span data-ttu-id="f0788-109">Hämta konfigurations post för offentliga underhåll</span><span class="sxs-lookup"><span data-stu-id="f0788-109">Get Public Maintenance configuration record</span></span>

## <span data-ttu-id="f0788-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0788-110">PARAMETERS</span></span>

### <span data-ttu-id="f0788-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0788-111">-DefaultProfile</span></span>
<span data-ttu-id="f0788-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f0788-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0788-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="f0788-113">-Name</span></span>
<span data-ttu-id="f0788-114">Konfigurations namnet för offentliga underhåll.</span><span class="sxs-lookup"><span data-stu-id="f0788-114">The public maintenance configuration Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0788-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0788-115">-ResourceGroupName</span></span>
<span data-ttu-id="f0788-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="f0788-116">The resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0788-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0788-117">CommonParameters</span></span>
<span data-ttu-id="f0788-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0788-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0788-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0788-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0788-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0788-120">INPUTS</span></span>

### <span data-ttu-id="f0788-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f0788-121">System.String</span></span>

## <span data-ttu-id="f0788-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0788-122">OUTPUTS</span></span>

### <span data-ttu-id="f0788-123">Microsoft. Azure. commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0788-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="f0788-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0788-124">NOTES</span></span>

## <span data-ttu-id="f0788-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0788-125">RELATED LINKS</span></span>