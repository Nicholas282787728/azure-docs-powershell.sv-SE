---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 630dc1a3a14beec147dec3f7bd2601ed0666ad78
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271451"
---
# <span data-ttu-id="75de3-101">Copy-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="75de3-101">Copy-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="75de3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75de3-102">SYNOPSIS</span></span>
<span data-ttu-id="75de3-103">Kopierar data från ett valv i en region till ett valv i en annan region.</span><span class="sxs-lookup"><span data-stu-id="75de3-103">Copies data from a vault in one region to a vault in another region.</span></span>

## <span data-ttu-id="75de3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75de3-104">SYNTAX</span></span>

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## <span data-ttu-id="75de3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75de3-105">DESCRIPTION</span></span>
<span data-ttu-id="75de3-106">Cmdleten **copy-AzRecoveryServicesVault** kopierar data från ett valv i en region till ett valv i en annan region.</span><span class="sxs-lookup"><span data-stu-id="75de3-106">The **Copy-AzRecoveryServicesVault** cmdlet copies data from a vault in one region to a vault in another region.</span></span> <span data-ttu-id="75de3-107">För närvarande stöds endast flytt av data på valv nivå.</span><span class="sxs-lookup"><span data-stu-id="75de3-107">Currently we only support vault level data move.</span></span>

## <span data-ttu-id="75de3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75de3-108">EXAMPLES</span></span>

### <span data-ttu-id="75de3-109">Exempel 1: kopiera data från vault1 till vault2</span><span class="sxs-lookup"><span data-stu-id="75de3-109">Example 1: Copy data from vault1 to vault2</span></span>
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a complete data move from vault1 to vault2. 

### Example 2: Copy data from vault1 to vault2 with only failed items
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

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

### <span data-ttu-id="75de3-110">-Force</span><span class="sxs-lookup"><span data-stu-id="75de3-110">-Force</span></span>
<span data-ttu-id="75de3-111">Tvingar åtgärden att flytta data (förhindrar bekräftelse dialog rutan) utan att fråga bekräfta den typ av redundans för mål valv som krävs.</span><span class="sxs-lookup"><span data-stu-id="75de3-111">Forces the data move operation (prevents confirmation dialog) without asking confirmation for target vault storage redundancy type.</span></span> <span data-ttu-id="75de3-112">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="75de3-112">This parameter is optional.</span></span> 

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

### <span data-ttu-id="75de3-113">-RetryOnlyFailed</span><span class="sxs-lookup"><span data-stu-id="75de3-113">-RetryOnlyFailed</span></span>
<span data-ttu-id="75de3-114">Växla parameter för att försöka flytta data bara för behållare i käll valvet som ännu inte har flyttats.</span><span class="sxs-lookup"><span data-stu-id="75de3-114">Switch parameter to try data move only for containers in the source vault which are not yet moved.</span></span>

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

### <span data-ttu-id="75de3-115">-SourceVault</span><span class="sxs-lookup"><span data-stu-id="75de3-115">-SourceVault</span></span>
<span data-ttu-id="75de3-116">Det käll valv objekt som ska flyttas.</span><span class="sxs-lookup"><span data-stu-id="75de3-116">The source vault object to be moved.</span></span>

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

### <span data-ttu-id="75de3-117">-TargetVault</span><span class="sxs-lookup"><span data-stu-id="75de3-117">-TargetVault</span></span>
<span data-ttu-id="75de3-118">Målobjektet som data ska flyttas till.</span><span class="sxs-lookup"><span data-stu-id="75de3-118">The target vault object where the data has to be moved.</span></span>

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

### <span data-ttu-id="75de3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75de3-119">CommonParameters</span></span>
<span data-ttu-id="75de3-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75de3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75de3-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75de3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75de3-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75de3-122">INPUTS</span></span>

### <span data-ttu-id="75de3-123">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="75de3-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="75de3-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75de3-124">OUTPUTS</span></span>

### <span data-ttu-id="75de3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="75de3-125">System.String</span></span>

## <span data-ttu-id="75de3-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75de3-126">NOTES</span></span>

## <span data-ttu-id="75de3-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75de3-127">RELATED LINKS</span></span>
