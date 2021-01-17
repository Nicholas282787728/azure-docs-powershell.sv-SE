---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: cdde8169c4b068b986910dc3bfc5de446833f5ff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421227"
---
# <span data-ttu-id="b25a0-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b25a0-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="b25a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b25a0-102">SYNOPSIS</span></span>
<span data-ttu-id="b25a0-103">Uppdaterar MSI till Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="b25a0-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="b25a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b25a0-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b25a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b25a0-105">DESCRIPTION</span></span>
<span data-ttu-id="b25a0-106">Denna cmdlet används för att lägga till eller ta bort MSI från Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="b25a0-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="b25a0-107">Använd-IdentityType parameter för att tilldela en SystemAssigned-identitet till RSVault.</span><span class="sxs-lookup"><span data-stu-id="b25a0-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="b25a0-108">Använd IdentityType none för att ta bort MSI från valvet.</span><span class="sxs-lookup"><span data-stu-id="b25a0-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="b25a0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b25a0-109">EXAMPLES</span></span>

### <span data-ttu-id="b25a0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b25a0-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="b25a0-111">Denna cmdlet används för att lägga till en SystemAssigned-identitet i ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="b25a0-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="b25a0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b25a0-112">PARAMETERS</span></span>

### <span data-ttu-id="b25a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b25a0-113">-DefaultProfile</span></span>
<span data-ttu-id="b25a0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b25a0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b25a0-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b25a0-115">-Name</span></span>

<span data-ttu-id="b25a0-116">Anger namnet på det Recovery-valv som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="b25a0-116">Specifies the name of the recovery services vault to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25a0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b25a0-117">-ResourceGroupName</span></span>

<span data-ttu-id="b25a0-118">Anger namnet på Azure Resource Group där Recovery Services-valvet finns.</span><span class="sxs-lookup"><span data-stu-id="b25a0-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25a0-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="b25a0-119">-IdentityType</span></span>
<span data-ttu-id="b25a0-120">MSI-typen som tilldelats Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="b25a0-120">The MSI type assigned to Recovery Services Vault.</span></span>

```yaml
Type: MSIdentity
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25a0-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b25a0-121">-Confirm</span></span>
<span data-ttu-id="b25a0-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b25a0-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25a0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b25a0-123">-WhatIf</span></span>
<span data-ttu-id="b25a0-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b25a0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b25a0-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b25a0-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25a0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b25a0-126">CommonParameters</span></span>
<span data-ttu-id="b25a0-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b25a0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b25a0-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b25a0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b25a0-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b25a0-129">INPUTS</span></span>

### <span data-ttu-id="b25a0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b25a0-130">System.String</span></span>

## <span data-ttu-id="b25a0-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b25a0-131">OUTPUTS</span></span>

### <span data-ttu-id="b25a0-132">Microsoft. Azure. Management. RecoveryServices. Models. valv</span><span class="sxs-lookup"><span data-stu-id="b25a0-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="b25a0-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b25a0-133">NOTES</span></span>

## <span data-ttu-id="b25a0-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b25a0-134">RELATED LINKS</span></span>
