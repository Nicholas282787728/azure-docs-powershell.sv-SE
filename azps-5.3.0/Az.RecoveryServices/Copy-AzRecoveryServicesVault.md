---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 68c2914c694dbfb89044597fc35582a83f426b6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521756"
---
# <span data-ttu-id="b0060-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b0060-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="b0060-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0060-102">SYNOPSIS</span></span>
<span data-ttu-id="b0060-103">Kopierar data från ett valv i en region till ett valv i en annan region.</span><span class="sxs-lookup"><span data-stu-id="b0060-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="b0060-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0060-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="b0060-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0060-105">DESCRIPTION</span></span>
<span data-ttu-id="b0060-106">Cmdleten **copy-AzRecoveryServicesVault** kopierar data från ett valv i en region till ett valv i en annan region.</span><span class="sxs-lookup"><span data-stu-id="b0060-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="b0060-107">För närvarande stöds endast flytt av data på valv nivå.</span><span class="sxs-lookup"><span data-stu-id="b0060-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="b0060-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0060-108">EXAMPLES</span></span>

### <span data-ttu-id="b0060-109">Exempel 1: kopiera data från vault1 till vault2</span><span class="sxs-lookup"><span data-stu-id="b0060-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

<span data-ttu-id="b0060-110">De första två cmdletarna Hämta Recovery Services-valvet-vault1 och vault2.</span><span class="sxs-lookup"><span data-stu-id="b0060-110">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="b0060-111">Med det andra kommandot utlöses en fullständig data förflyttning från vault1 till vault2.</span><span class="sxs-lookup"><span data-stu-id="b0060-111">The second command triggers a complete data move from vault1 to vault2.</span></span> 

### <span data-ttu-id="b0060-112">Exempel 2: kopiera data från vault1 till vault2 med bara misslyckade objekt</span><span class="sxs-lookup"><span data-stu-id="b0060-112">Example 2: Copy data from vault1 to vault2 with only failed items</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
``` 

<span data-ttu-id="b0060-113">De första två cmdletarna Hämta Recovery Services-valvet-vault1 och vault2.</span><span class="sxs-lookup"><span data-stu-id="b0060-113">The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.</span></span>
<span data-ttu-id="b0060-114">Med det andra kommandot utlöses en del data från vault1 till vault2 med bara de objekt som inte kunde flyttas.</span><span class="sxs-lookup"><span data-stu-id="b0060-114">The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.</span></span>

## <span data-ttu-id="b0060-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0060-115">PARAMETERS</span></span>

### <span data-ttu-id="b0060-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0060-116">-DefaultProfile</span></span>
<span data-ttu-id="b0060-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0060-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0060-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b0060-118">-Force</span></span>
<span data-ttu-id="b0060-119">Tvingar åtgärden att flytta data (förhindrar bekräftelse dialog rutan) utan att fråga bekräfta den typ av redundans för mål valv som krävs.</span><span class="sxs-lookup"><span data-stu-id="b0060-119">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="b0060-120">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b0060-120">This parameter is optional.</span></span> 

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0060-121">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="b0060-121">-RetryOnlyFailed</span></span>
<span data-ttu-id="b0060-122">Växla parameter för att försöka flytta data bara för behållare i käll valvet som ännu inte har flyttats.</span><span class="sxs-lookup"><span data-stu-id="b0060-122">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0060-123">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="b0060-123">-SourceVault</span></span>
<span data-ttu-id="b0060-124">Det käll valv objekt som ska flyttas.</span><span class="sxs-lookup"><span data-stu-id="b0060-124">The source vault object to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0060-125">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="b0060-125">-TargetVault</span></span>
<span data-ttu-id="b0060-126">Målobjektet som data ska flyttas till.</span><span class="sxs-lookup"><span data-stu-id="b0060-126">The target vault object where the data has to be moved.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0060-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0060-127">CommonParameters</span></span>
<span data-ttu-id="b0060-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0060-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0060-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0060-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0060-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0060-130">INPUTS</span></span>

### <span data-ttu-id="b0060-131">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="b0060-131">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="b0060-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0060-132">OUTPUTS</span></span>

### <span data-ttu-id="b0060-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b0060-133">System.String</span></span>

## <span data-ttu-id="b0060-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0060-134">NOTES</span></span>

## <span data-ttu-id="b0060-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0060-135">RELATED LINKS</span></span>
