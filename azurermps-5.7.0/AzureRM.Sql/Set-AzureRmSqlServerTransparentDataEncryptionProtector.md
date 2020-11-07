---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: d78b6931e58469b20b2b937de083ff9d96f3f92d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574143"
---
# <span data-ttu-id="9432c-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="9432c-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="9432c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9432c-102">SYNOPSIS</span></span>
<span data-ttu-id="9432c-103">Ställer in skydd mot transparent data kryptering (TDE) för en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="9432c-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9432c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9432c-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9432c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9432c-105">DESCRIPTION</span></span>
<span data-ttu-id="9432c-106">Set-AzureRmSqlServerTransparentDataEncryptionProtector-cmdleten ställer in TDE-skyddskomponenten för en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="9432c-106">The Set-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="9432c-107">Om du ändrar TDE skydds typ roteras skydds komponenten.</span><span class="sxs-lookup"><span data-stu-id="9432c-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="9432c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9432c-108">EXAMPLES</span></span>

### <span data-ttu-id="9432c-109">Exempel 1: Ange skydds typen transparent Data Encryption (TDE) till ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="9432c-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="9432c-110">Det här kommandot uppdaterar en servers TDE skydds typ till tjänst hanterad.</span><span class="sxs-lookup"><span data-stu-id="9432c-110">This command updates a server's TDE protector type to Service Managed.</span></span>

<span data-ttu-id="9432c-111">ResourceGroupName ServerName ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="9432c-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="9432c-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="9432c-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="9432c-113">Exempel 2: Ange den transparenta typen av data krypterings skydd för Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="9432c-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="9432c-114">Det här kommandot uppdaterar en server för användning av Server Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' som TDE-skydd.</span><span class="sxs-lookup"><span data-stu-id="9432c-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

<span data-ttu-id="9432c-115">ResourceGroupName ServerName ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="9432c-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="9432c-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="9432c-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="9432c-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9432c-117">PARAMETERS</span></span>

### <span data-ttu-id="9432c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9432c-118">-AsJob</span></span>
<span data-ttu-id="9432c-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9432c-119">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9432c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9432c-120">-DefaultProfile</span></span>
<span data-ttu-id="9432c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9432c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9432c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9432c-122">-Force</span></span>
<span data-ttu-id="9432c-123">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="9432c-123">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9432c-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="9432c-124">-KeyId</span></span>
<span data-ttu-id="9432c-125">KeyId för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9432c-125">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9432c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9432c-126">-ResourceGroupName</span></span>
<span data-ttu-id="9432c-127">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="9432c-127">The name of the resource group</span></span>

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

### <span data-ttu-id="9432c-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9432c-128">-ServerName</span></span>
<span data-ttu-id="9432c-129">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="9432c-129">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9432c-130">– Skriv</span><span class="sxs-lookup"><span data-stu-id="9432c-130">-Type</span></span>
<span data-ttu-id="9432c-131">TDE skydds typ för Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="9432c-131">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9432c-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9432c-132">-Confirm</span></span>
<span data-ttu-id="9432c-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9432c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9432c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9432c-134">-WhatIf</span></span>
<span data-ttu-id="9432c-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9432c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9432c-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9432c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9432c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9432c-137">CommonParameters</span></span>
<span data-ttu-id="9432c-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9432c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9432c-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9432c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9432c-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9432c-140">INPUTS</span></span>

### <span data-ttu-id="9432c-141">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="9432c-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>
<span data-ttu-id="9432c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9432c-142">System.String</span></span>

## <span data-ttu-id="9432c-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9432c-143">OUTPUTS</span></span>

### <span data-ttu-id="9432c-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="9432c-144">System.Object</span></span>

## <span data-ttu-id="9432c-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9432c-145">NOTES</span></span>

## <span data-ttu-id="9432c-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9432c-146">RELATED LINKS</span></span>

[<span data-ttu-id="9432c-147">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="9432c-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)