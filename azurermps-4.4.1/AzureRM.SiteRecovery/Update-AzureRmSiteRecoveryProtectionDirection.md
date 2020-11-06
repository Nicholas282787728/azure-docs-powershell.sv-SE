---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: 6103e9a820a80df7e89130f269296cd073283947
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575792"
---
# <span data-ttu-id="ded6b-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="ded6b-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="ded6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ded6b-102">SYNOPSIS</span></span>
<span data-ttu-id="ded6b-103">Uppdaterar käll-och mål servern för att skydda ett webbplats återställnings objekt.</span><span class="sxs-lookup"><span data-stu-id="ded6b-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ded6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ded6b-104">SYNTAX</span></span>

### <span data-ttu-id="ded6b-105">ByPEObject (standard)</span><span class="sxs-lookup"><span data-stu-id="ded6b-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ded6b-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="ded6b-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ded6b-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="ded6b-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ded6b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ded6b-108">DESCRIPTION</span></span>
<span data-ttu-id="ded6b-109">Cmdleten **Update-AzureRmSiteRecoveryProtectionDirection** uppdaterar käll-och mål servern för att skydda ett Azure Site Recovery-objekt efter att commit failover-åtgärden slutförts.</span><span class="sxs-lookup"><span data-stu-id="ded6b-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="ded6b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ded6b-110">EXAMPLES</span></span>

## <span data-ttu-id="ded6b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ded6b-111">PARAMETERS</span></span>

### <span data-ttu-id="ded6b-112">-Riktning</span><span class="sxs-lookup"><span data-stu-id="ded6b-112">-Direction</span></span>
<span data-ttu-id="ded6b-113">Anger riktningen för bekräftelsen.</span><span class="sxs-lookup"><span data-stu-id="ded6b-113">Specifies the direction of the commit.</span></span>
<span data-ttu-id="ded6b-114">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ded6b-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ded6b-115">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="ded6b-115">PrimaryToRecovery</span></span>
- <span data-ttu-id="ded6b-116">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="ded6b-116">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ded6b-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ded6b-117">-ProtectionEntity</span></span>
<span data-ttu-id="ded6b-118">Anger objektet skydd.</span><span class="sxs-lookup"><span data-stu-id="ded6b-118">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ded6b-119">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ded6b-119">-RecoveryPlan</span></span>
<span data-ttu-id="ded6b-120">Anger ett återställnings plan objekt.</span><span class="sxs-lookup"><span data-stu-id="ded6b-120">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ded6b-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ded6b-121">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ded6b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded6b-122">-DefaultProfile</span></span>
<span data-ttu-id="ded6b-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ded6b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ded6b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded6b-124">CommonParameters</span></span>
<span data-ttu-id="ded6b-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ded6b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded6b-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ded6b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded6b-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ded6b-127">INPUTS</span></span>

### <span data-ttu-id="ded6b-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ded6b-128">ASRProtectionEntity</span></span>
<span data-ttu-id="ded6b-129">Parametern ' ProtectionEntity ' godkänner värdet av typen ' ASRProtectionEntity ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ded6b-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="ded6b-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ded6b-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="ded6b-131">Parametern ' RecoveryPlan ' godkänner värdet av typen ' ASRRecoveryPlan ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ded6b-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="ded6b-132">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ded6b-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="ded6b-133">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ded6b-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="ded6b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ded6b-134">OUTPUTS</span></span>

### <span data-ttu-id="ded6b-135">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ded6b-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ded6b-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ded6b-136">NOTES</span></span>

## <span data-ttu-id="ded6b-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ded6b-137">RELATED LINKS</span></span>

