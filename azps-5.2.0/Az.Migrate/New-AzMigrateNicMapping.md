---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408947"
---
# <span data-ttu-id="51bae-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="51bae-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="51bae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51bae-102">SYNOPSIS</span></span>
<span data-ttu-id="51bae-103">Skapar ett objekt som uppdaterar NIC-egenskaper för en replikerande Server.</span><span class="sxs-lookup"><span data-stu-id="51bae-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="51bae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51bae-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="51bae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51bae-105">DESCRIPTION</span></span>
<span data-ttu-id="51bae-106">New-AzMigrateNicMapping-cmdleten skapar en mappning av det käll nätverkskort som är kopplat till servern som ska migreras.</span><span class="sxs-lookup"><span data-stu-id="51bae-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="51bae-107">Det här objektet tillhandahålls som en inmatning till Set-AzMigrateServerReplication cmdlet för att uppdatera kortet och dess egenskaper för en replikerande Server.</span><span class="sxs-lookup"><span data-stu-id="51bae-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="51bae-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51bae-108">EXAMPLES</span></span>

### <span data-ttu-id="51bae-109">Exempel 1: skapa ett NIC-objekt</span><span class="sxs-lookup"><span data-stu-id="51bae-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="51bae-110">Skapar ett NIC-uppdateringsfiler.</span><span class="sxs-lookup"><span data-stu-id="51bae-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="51bae-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51bae-111">PARAMETERS</span></span>

### <span data-ttu-id="51bae-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="51bae-112">-NicID</span></span>
<span data-ttu-id="51bae-113">Anger ID för det nätverkskort som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="51bae-113">Specifies the ID of the NIC to be updated.</span></span>

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

### <span data-ttu-id="51bae-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="51bae-114">-TargetNicIP</span></span>
<span data-ttu-id="51bae-115">Anger IP-adressen i mål under nätet som ska användas för NÄTVERKSKORTet.</span><span class="sxs-lookup"><span data-stu-id="51bae-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

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

### <span data-ttu-id="51bae-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="51bae-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="51bae-117">Anger om det nätverkskort som ska uppdateras ska vara primärt, sekundärt eller inte migrerat.</span><span class="sxs-lookup"><span data-stu-id="51bae-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

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

### <span data-ttu-id="51bae-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="51bae-118">-TargetNicSubnet</span></span>
<span data-ttu-id="51bae-119">Anger nät namnet på NÄTVERKSKORTet i det virtuella mål nätverket som servern måste migreras till.</span><span class="sxs-lookup"><span data-stu-id="51bae-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="51bae-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51bae-120">CommonParameters</span></span>
<span data-ttu-id="51bae-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51bae-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51bae-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51bae-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51bae-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51bae-123">INPUTS</span></span>

## <span data-ttu-id="51bae-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51bae-124">OUTPUTS</span></span>

### <span data-ttu-id="51bae-125">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="51bae-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="51bae-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51bae-126">NOTES</span></span>

<span data-ttu-id="51bae-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="51bae-127">ALIASES</span></span>

## <span data-ttu-id="51bae-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51bae-128">RELATED LINKS</span></span>

