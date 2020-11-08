---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 3bb602d148b0843def129a1e4538d9ef8fdbe169
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261985"
---
# <span data-ttu-id="9818a-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9818a-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="9818a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9818a-102">SYNOPSIS</span></span>
<span data-ttu-id="9818a-103">Skapar ett nytt Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="9818a-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="9818a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9818a-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9818a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9818a-105">DESCRIPTION</span></span>
<span data-ttu-id="9818a-106">Cmdleten **New-AzRecoveryServicesVault** skapar ett nytt Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="9818a-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="9818a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9818a-107">EXAMPLES</span></span>

### <span data-ttu-id="9818a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9818a-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="9818a-109">Skapa ett valv för återställnings tjänster i resurs gruppen och den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="9818a-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="9818a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9818a-110">PARAMETERS</span></span>

### <span data-ttu-id="9818a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9818a-111">-DefaultProfile</span></span>
<span data-ttu-id="9818a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9818a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9818a-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="9818a-113">-Location</span></span>
<span data-ttu-id="9818a-114">Anger namnet på den geografiska platsen för valvet.</span><span class="sxs-lookup"><span data-stu-id="9818a-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="9818a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9818a-115">-Name</span></span>
<span data-ttu-id="9818a-116">Anger namnet på det valv som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="9818a-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="9818a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9818a-117">-ResourceGroupName</span></span>
<span data-ttu-id="9818a-118">Anger namnet på den Azure-adressresurs som du vill skapa eller från vilken det angivna Recovery Services-objektet ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="9818a-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="9818a-119">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9818a-119">-Tag</span></span>

<span data-ttu-id="9818a-120">Anger taggarna som ska läggas till i Recovery Services-valvet</span><span class="sxs-lookup"><span data-stu-id="9818a-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9818a-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9818a-121">-Confirm</span></span>
<span data-ttu-id="9818a-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9818a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9818a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9818a-123">-WhatIf</span></span>
<span data-ttu-id="9818a-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9818a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9818a-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9818a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9818a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9818a-126">CommonParameters</span></span>
<span data-ttu-id="9818a-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9818a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9818a-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9818a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9818a-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9818a-129">INPUTS</span></span>

### <span data-ttu-id="9818a-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="9818a-130">None</span></span>

## <span data-ttu-id="9818a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9818a-131">OUTPUTS</span></span>

### <span data-ttu-id="9818a-132">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="9818a-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="9818a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9818a-133">NOTES</span></span>

## <span data-ttu-id="9818a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9818a-134">RELATED LINKS</span></span>

[<span data-ttu-id="9818a-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9818a-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="9818a-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9818a-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="9818a-137">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9818a-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


