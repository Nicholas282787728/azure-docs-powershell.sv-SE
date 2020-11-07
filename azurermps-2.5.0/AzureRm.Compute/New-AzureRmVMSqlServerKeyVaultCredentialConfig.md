---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
ms.openlocfilehash: ee627065d1d6be8037d1a9b054ec6452b9becb41
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930702"
---
# <span data-ttu-id="10e6b-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="10e6b-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="10e6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="10e6b-103">Skapar ett konfigurations objekt för SQL Server Key valv-autentiseringsuppgifter på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="10e6b-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10e6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10e6b-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10e6b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10e6b-105">DESCRIPTION</span></span>

## <span data-ttu-id="10e6b-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10e6b-106">EXAMPLES</span></span>

## <span data-ttu-id="10e6b-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10e6b-107">PARAMETERS</span></span>

### <span data-ttu-id="10e6b-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="10e6b-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e6b-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="10e6b-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e6b-110">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="10e6b-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e6b-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10e6b-111">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e6b-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="10e6b-112">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e6b-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="10e6b-113">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e6b-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="10e6b-114">-Confirm</span></span>
<span data-ttu-id="10e6b-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="10e6b-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10e6b-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10e6b-116">-WhatIf</span></span>
<span data-ttu-id="10e6b-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="10e6b-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="10e6b-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="10e6b-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10e6b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e6b-119">CommonParameters</span></span>
<span data-ttu-id="10e6b-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10e6b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e6b-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10e6b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e6b-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10e6b-122">INPUTS</span></span>

### <span data-ttu-id="10e6b-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="10e6b-123">None</span></span>
<span data-ttu-id="10e6b-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="10e6b-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="10e6b-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10e6b-125">OUTPUTS</span></span>

### <span data-ttu-id="10e6b-126">Microsoft. Azure. commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="10e6b-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="10e6b-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10e6b-127">NOTES</span></span>

## <span data-ttu-id="10e6b-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10e6b-128">RELATED LINKS</span></span>

