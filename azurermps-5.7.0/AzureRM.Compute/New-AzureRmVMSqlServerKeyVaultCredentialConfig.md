---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 4e252001d1459c52a35b766d34c91050df62073d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576607"
---
# <span data-ttu-id="2c416-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="2c416-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="2c416-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c416-102">SYNOPSIS</span></span>
<span data-ttu-id="2c416-103">Skapar ett konfigurations objekt för SQL Server Key valv-autentiseringsuppgifter på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2c416-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c416-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c416-104">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c416-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c416-105">DESCRIPTION</span></span>

## <span data-ttu-id="2c416-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c416-106">EXAMPLES</span></span>

## <span data-ttu-id="2c416-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c416-107">PARAMETERS</span></span>

### <span data-ttu-id="2c416-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="2c416-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="2c416-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="2c416-109">-CredentialName</span></span>
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

### <span data-ttu-id="2c416-110">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="2c416-110">-Enable</span></span>
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

### <span data-ttu-id="2c416-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c416-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="2c416-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2c416-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="2c416-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="2c416-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="2c416-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c416-114">-Confirm</span></span>
<span data-ttu-id="2c416-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c416-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c416-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c416-116">-WhatIf</span></span>
<span data-ttu-id="2c416-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c416-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2c416-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c416-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c416-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c416-119">CommonParameters</span></span>
<span data-ttu-id="2c416-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c416-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c416-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c416-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c416-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c416-122">INPUTS</span></span>

### <span data-ttu-id="2c416-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="2c416-123">None</span></span>
<span data-ttu-id="2c416-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2c416-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2c416-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c416-125">OUTPUTS</span></span>

## <span data-ttu-id="2c416-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c416-126">NOTES</span></span>

## <span data-ttu-id="2c416-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c416-127">RELATED LINKS</span></span>

