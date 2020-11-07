---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 5d8f67de6b6bbe08a34dad279674b29befaa161c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745077"
---
# <span data-ttu-id="5d337-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="5d337-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="5d337-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d337-102">SYNOPSIS</span></span>
<span data-ttu-id="5d337-103">Skapar ett konfigurations objekt för SQL Server Key valv-autentiseringsuppgifter på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="5d337-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="5d337-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d337-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d337-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d337-105">DESCRIPTION</span></span>

## <span data-ttu-id="5d337-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d337-106">EXAMPLES</span></span>

## <span data-ttu-id="5d337-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d337-107">PARAMETERS</span></span>

### <span data-ttu-id="5d337-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="5d337-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="5d337-109">URL för Azure Key valv-tjänsten</span><span class="sxs-lookup"><span data-stu-id="5d337-109">Azure Key Vault service URL</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d337-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="5d337-110">-CredentialName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d337-111">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="5d337-111">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d337-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d337-112">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d337-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="5d337-113">-ServicePrincipalName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d337-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="5d337-114">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d337-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5d337-115">-Confirm</span></span>
<span data-ttu-id="5d337-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5d337-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d337-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d337-117">-WhatIf</span></span>
<span data-ttu-id="5d337-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5d337-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d337-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5d337-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d337-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d337-120">CommonParameters</span></span>
<span data-ttu-id="5d337-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d337-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d337-122">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d337-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d337-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d337-123">INPUTS</span></span>

### <span data-ttu-id="5d337-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5d337-124">System.String</span></span>

### <span data-ttu-id="5d337-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5d337-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5d337-126">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="5d337-126">System.Security.SecureString</span></span>

## <span data-ttu-id="5d337-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d337-127">OUTPUTS</span></span>

### <span data-ttu-id="5d337-128">Microsoft. Azure. commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="5d337-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="5d337-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d337-129">NOTES</span></span>

## <span data-ttu-id="5d337-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d337-130">RELATED LINKS</span></span>
