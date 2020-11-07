---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: dcb099a26fe46325b1c3869b5e507347c948f09f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920262"
---
# <span data-ttu-id="e8ba7-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e8ba7-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="e8ba7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ba7-103">Tar bort en Key Vault-tangenten från en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="e8ba7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8ba7-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8ba7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8ba7-105">DESCRIPTION</span></span>
<span data-ttu-id="e8ba7-106">Remove-AzSqlServerKeyVaultKey cmdlet tar bort Key Vault-tangenten från den angivna SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="e8ba7-107">Observera att SQL Server-behörigheterna till Key-valvet inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="e8ba7-108">Använd set-AzKeyVaultAccessPolicy för att ändra behörigheter.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="e8ba7-109">Observera att denna cmdlet inte gör några ändringar i huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="e8ba7-110">Använd Remove-AzKeyVaultKey om du vill ta bort en Key-valv.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="e8ba7-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8ba7-111">EXAMPLES</span></span>

### <span data-ttu-id="e8ba7-112">Exempel 1: ta bort en Key valv-tangenten</span><span class="sxs-lookup"><span data-stu-id="e8ba7-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="e8ba7-113">Det här kommandot tar bort Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' från den angivna servern.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="e8ba7-114">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 tumavtryck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="e8ba7-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="e8ba7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8ba7-115">PARAMETERS</span></span>

### <span data-ttu-id="e8ba7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8ba7-116">-AsJob</span></span>
<span data-ttu-id="e8ba7-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e8ba7-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ba7-118">-DefaultProfile</span></span>
<span data-ttu-id="e8ba7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e8ba7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8ba7-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="e8ba7-120">-KeyId</span></span>
<span data-ttu-id="e8ba7-121">KeyId för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-121">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ba7-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8ba7-123">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e8ba7-123">The name of the resource group</span></span>

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

### <span data-ttu-id="e8ba7-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e8ba7-124">-ServerName</span></span>
<span data-ttu-id="e8ba7-125">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-125">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ba7-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e8ba7-126">-Confirm</span></span>
<span data-ttu-id="e8ba7-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ba7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ba7-128">-WhatIf</span></span>
<span data-ttu-id="e8ba7-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8ba7-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ba7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ba7-131">CommonParameters</span></span>
<span data-ttu-id="e8ba7-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8ba7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ba7-133">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8ba7-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ba7-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8ba7-134">INPUTS</span></span>

### <span data-ttu-id="e8ba7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e8ba7-135">System.String</span></span>

## <span data-ttu-id="e8ba7-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8ba7-136">OUTPUTS</span></span>

### <span data-ttu-id="e8ba7-137">Microsoft. Azure. commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="e8ba7-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="e8ba7-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8ba7-138">NOTES</span></span>

## <span data-ttu-id="e8ba7-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8ba7-139">RELATED LINKS</span></span>

[<span data-ttu-id="e8ba7-140">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e8ba7-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
