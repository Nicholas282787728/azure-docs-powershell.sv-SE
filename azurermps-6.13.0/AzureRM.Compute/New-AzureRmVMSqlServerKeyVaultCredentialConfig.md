---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: dc1ea08b0770c7438574d4ef2cc6a97cb99f2909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756225"
---
# <span data-ttu-id="aa31d-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="aa31d-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="aa31d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa31d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa31d-103">Skapar ett konfigurations objekt för SQL Server Key valv-autentiseringsuppgifter på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="aa31d-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa31d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa31d-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa31d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa31d-105">DESCRIPTION</span></span>

## <span data-ttu-id="aa31d-106">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa31d-106">EXAMPLES</span></span>

## <span data-ttu-id="aa31d-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa31d-107">PARAMETERS</span></span>

### <span data-ttu-id="aa31d-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="aa31d-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="aa31d-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="aa31d-109">-CredentialName</span></span>
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

### <span data-ttu-id="aa31d-110">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="aa31d-110">-Enable</span></span>
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

### <span data-ttu-id="aa31d-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa31d-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="aa31d-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="aa31d-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="aa31d-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="aa31d-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="aa31d-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aa31d-114">-Confirm</span></span>
<span data-ttu-id="aa31d-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aa31d-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa31d-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa31d-116">-WhatIf</span></span>
<span data-ttu-id="aa31d-117">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aa31d-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa31d-118">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aa31d-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa31d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa31d-119">CommonParameters</span></span>
<span data-ttu-id="aa31d-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa31d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa31d-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa31d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa31d-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa31d-122">INPUTS</span></span>

### <span data-ttu-id="aa31d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="aa31d-123">System.String</span></span>

### <span data-ttu-id="aa31d-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aa31d-124">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="aa31d-125">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="aa31d-125">System.Security.SecureString</span></span>

## <span data-ttu-id="aa31d-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa31d-126">OUTPUTS</span></span>

### <span data-ttu-id="aa31d-127">Microsoft. Azure. commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="aa31d-127">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="aa31d-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa31d-128">NOTES</span></span>

## <span data-ttu-id="aa31d-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa31d-129">RELATED LINKS</span></span>
