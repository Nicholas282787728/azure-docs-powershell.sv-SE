---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: d2d2bd98491b5bf91aebb45e6b8a3368a58d1b56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746472"
---
# <span data-ttu-id="35154-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="35154-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="35154-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35154-102">SYNOPSIS</span></span>
<span data-ttu-id="35154-103">Ställer in skydd mot transparent data kryptering (TDE) för en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="35154-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="35154-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35154-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35154-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35154-105">DESCRIPTION</span></span>
<span data-ttu-id="35154-106">Set-AzSqlServerTransparentDataEncryptionProtector-cmdleten ställer in TDE-skyddskomponenten för en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="35154-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="35154-107">Om du ändrar TDE skydds typ roteras skydds komponenten.</span><span class="sxs-lookup"><span data-stu-id="35154-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="35154-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35154-108">EXAMPLES</span></span>

### <span data-ttu-id="35154-109">Exempel 1: Ange skydds typen transparent Data Encryption (TDE) till ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="35154-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="35154-110">Det här kommandot uppdaterar en servers TDE skydds typ till tjänst hanterad.</span><span class="sxs-lookup"><span data-stu-id="35154-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="35154-111">ResourceGroupName ServerName ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="35154-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="35154-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="35154-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="35154-113">Exempel 2: Ange den transparenta typen av data krypterings skydd för Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="35154-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="35154-114">Det här kommandot uppdaterar en server för användning av Server Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' som TDE-skydd.</span><span class="sxs-lookup"><span data-stu-id="35154-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="35154-115">ResourceGroupName ServerName ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="35154-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="35154-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="35154-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="35154-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35154-117">PARAMETERS</span></span>

### <span data-ttu-id="35154-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35154-118">-AsJob</span></span>
<span data-ttu-id="35154-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="35154-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35154-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35154-120">-DefaultProfile</span></span>
<span data-ttu-id="35154-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="35154-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35154-122">-Force</span><span class="sxs-lookup"><span data-stu-id="35154-122">-Force</span></span>
<span data-ttu-id="35154-123">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="35154-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="35154-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="35154-124">-KeyId</span></span>
<span data-ttu-id="35154-125">KeyId för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="35154-125">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35154-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35154-126">-ResourceGroupName</span></span>
<span data-ttu-id="35154-127">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="35154-127">The name of the resource group</span></span>

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

### <span data-ttu-id="35154-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="35154-128">-ServerName</span></span>
<span data-ttu-id="35154-129">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="35154-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="35154-130">– Skriv</span><span class="sxs-lookup"><span data-stu-id="35154-130">-Type</span></span>
<span data-ttu-id="35154-131">TDE skydds typ för Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="35154-131">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35154-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="35154-132">-Confirm</span></span>
<span data-ttu-id="35154-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="35154-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35154-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35154-134">-WhatIf</span></span>
<span data-ttu-id="35154-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="35154-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35154-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="35154-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35154-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35154-137">CommonParameters</span></span>
<span data-ttu-id="35154-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35154-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35154-139">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35154-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35154-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35154-140">INPUTS</span></span>

### <span data-ttu-id="35154-141">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="35154-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="35154-142">System. String</span><span class="sxs-lookup"><span data-stu-id="35154-142">System.String</span></span>

## <span data-ttu-id="35154-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35154-143">OUTPUTS</span></span>

### <span data-ttu-id="35154-144">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="35154-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="35154-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35154-145">NOTES</span></span>

## <span data-ttu-id="35154-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35154-146">RELATED LINKS</span></span>

[<span data-ttu-id="35154-147">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="35154-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
