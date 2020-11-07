---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: 3607835496aa6f99cfd2b42383654180d6b12331
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919724"
---
# <span data-ttu-id="a7178-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a7178-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="a7178-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a7178-102">SYNOPSIS</span></span>

<span data-ttu-id="a7178-103">Hämtar en lista över återställnings tjänstens valv.</span><span class="sxs-lookup"><span data-stu-id="a7178-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="a7178-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a7178-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7178-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a7178-105">DESCRIPTION</span></span>

<span data-ttu-id="a7178-106">Cmdleten **Get-AzRecoveryServicesVault** hämtar en lista över återställnings tjänst valv i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a7178-106">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="a7178-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a7178-107">EXAMPLES</span></span>

### <span data-ttu-id="a7178-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a7178-108">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="a7178-109">Hämta listan med valv i det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a7178-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="a7178-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a7178-110">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="a7178-111">Hämta listan med valv i resurs gruppen i det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a7178-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="a7178-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a7178-112">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="a7178-113">Hämta valvet i resurs gruppen med angivet namn.</span><span class="sxs-lookup"><span data-stu-id="a7178-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="a7178-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a7178-114">PARAMETERS</span></span>

### <span data-ttu-id="a7178-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7178-115">-DefaultProfile</span></span>

<span data-ttu-id="a7178-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a7178-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7178-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a7178-117">-Name</span></span>

<span data-ttu-id="a7178-118">Anger namnet på valvet du vill fråga efter.</span><span class="sxs-lookup"><span data-stu-id="a7178-118">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="a7178-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7178-119">-ResourceGroupName</span></span>

<span data-ttu-id="a7178-120">Anger namnet på den Azure Resource-grupp från vilken det angivna Recovery Services-objektet ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="a7178-120">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="a7178-121">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7178-121">-CommonParameters</span></span>

<span data-ttu-id="a7178-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7178-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7178-123">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7178-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7178-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a7178-124">INPUTS</span></span>

### <span data-ttu-id="a7178-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="a7178-125">None</span></span>

## <span data-ttu-id="a7178-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a7178-126">OUTPUTS</span></span>

### <span data-ttu-id="a7178-127">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="a7178-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a7178-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a7178-128">NOTES</span></span>

## <span data-ttu-id="a7178-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a7178-129">RELATED LINKS</span></span>

[<span data-ttu-id="a7178-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a7178-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="a7178-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a7178-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="a7178-132">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a7178-132">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
