---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b93167e0e0a089595cb45710072c670c1cdb7af0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927110"
---
# <span data-ttu-id="94f26-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="94f26-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="94f26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94f26-102">SYNOPSIS</span></span>
<span data-ttu-id="94f26-103">Ställer in skydd mot transparent data kryptering (TDE) för en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="94f26-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="94f26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94f26-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f26-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94f26-105">DESCRIPTION</span></span>
<span data-ttu-id="94f26-106">Set-AzSqlServerTransparentDataEncryptionProtector-cmdleten ställer in TDE-skyddskomponenten för en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="94f26-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="94f26-107">Om du ändrar TDE skydds typ roteras skydds komponenten.</span><span class="sxs-lookup"><span data-stu-id="94f26-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="94f26-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94f26-108">EXAMPLES</span></span>

### <span data-ttu-id="94f26-109">Exempel 1: Ange skydds typen transparent Data Encryption (TDE) till ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="94f26-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="94f26-110">Det här kommandot uppdaterar en servers TDE skydds typ till tjänst hanterad.</span><span class="sxs-lookup"><span data-stu-id="94f26-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="94f26-111">ResourceGroupName ServerName ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="94f26-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="94f26-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="94f26-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="94f26-113">Exempel 2: Ange den transparenta typen av data krypterings skydd för Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="94f26-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="94f26-114">Det här kommandot uppdaterar en server för användning av Server Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' som TDE-skydd.</span><span class="sxs-lookup"><span data-stu-id="94f26-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="94f26-115">ResourceGroupName ServerName ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="94f26-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="94f26-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="94f26-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="94f26-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94f26-117">PARAMETERS</span></span>

### <span data-ttu-id="94f26-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94f26-118">-AsJob</span></span>
<span data-ttu-id="94f26-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="94f26-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94f26-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f26-120">-DefaultProfile</span></span>
<span data-ttu-id="94f26-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="94f26-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94f26-122">-Force</span><span class="sxs-lookup"><span data-stu-id="94f26-122">-Force</span></span>
<span data-ttu-id="94f26-123">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="94f26-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="94f26-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="94f26-124">-KeyId</span></span>
<span data-ttu-id="94f26-125">KeyId för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="94f26-125">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="94f26-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f26-126">-ResourceGroupName</span></span>
<span data-ttu-id="94f26-127">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="94f26-127">The name of the resource group</span></span>

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

### <span data-ttu-id="94f26-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="94f26-128">-ServerName</span></span>
<span data-ttu-id="94f26-129">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="94f26-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="94f26-130">– Skriv</span><span class="sxs-lookup"><span data-stu-id="94f26-130">-Type</span></span>
<span data-ttu-id="94f26-131">TDE skydds typ för Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="94f26-131">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="94f26-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="94f26-132">-Confirm</span></span>
<span data-ttu-id="94f26-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94f26-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f26-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f26-134">-WhatIf</span></span>
<span data-ttu-id="94f26-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="94f26-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94f26-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="94f26-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f26-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f26-137">CommonParameters</span></span>
<span data-ttu-id="94f26-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f26-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f26-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94f26-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f26-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94f26-140">INPUTS</span></span>

### <span data-ttu-id="94f26-141">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="94f26-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="94f26-142">System. String</span><span class="sxs-lookup"><span data-stu-id="94f26-142">System.String</span></span>

## <span data-ttu-id="94f26-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94f26-143">OUTPUTS</span></span>

### <span data-ttu-id="94f26-144">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="94f26-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="94f26-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94f26-145">NOTES</span></span>

## <span data-ttu-id="94f26-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94f26-146">RELATED LINKS</span></span>

[<span data-ttu-id="94f26-147">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="94f26-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
