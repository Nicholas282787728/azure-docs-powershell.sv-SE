---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: d9f732a40b61687d7970fdf24f9f9f0f841b2cc7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925041"
---
# <span data-ttu-id="edfff-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="edfff-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="edfff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="edfff-102">SYNOPSIS</span></span>
<span data-ttu-id="edfff-103">Skapar ett konfigurations objekt för SQL Server Key valv-autentiseringsuppgifter på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="edfff-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="edfff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="edfff-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edfff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="edfff-105">DESCRIPTION</span></span>

## <span data-ttu-id="edfff-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="edfff-106">EXAMPLES</span></span>

## <span data-ttu-id="edfff-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="edfff-107">PARAMETERS</span></span>

### <span data-ttu-id="edfff-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="edfff-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="edfff-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="edfff-109">-CredentialName</span></span>
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

### <span data-ttu-id="edfff-110">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="edfff-110">-Enable</span></span>
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

### <span data-ttu-id="edfff-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edfff-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="edfff-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="edfff-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="edfff-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="edfff-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="edfff-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="edfff-114">-Confirm</span></span>
<span data-ttu-id="edfff-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="edfff-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edfff-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edfff-116">-WhatIf</span></span>
<span data-ttu-id="edfff-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="edfff-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="edfff-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="edfff-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edfff-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edfff-119">CommonParameters</span></span>
<span data-ttu-id="edfff-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edfff-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edfff-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edfff-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edfff-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="edfff-122">INPUTS</span></span>

### <span data-ttu-id="edfff-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="edfff-123">None</span></span>
<span data-ttu-id="edfff-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="edfff-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="edfff-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="edfff-125">OUTPUTS</span></span>

### <span data-ttu-id="edfff-126">Microsoft. Azure. commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="edfff-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="edfff-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="edfff-127">NOTES</span></span>

## <span data-ttu-id="edfff-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="edfff-128">RELATED LINKS</span></span>

