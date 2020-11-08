---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: a736ede2c84b3fbe782928d7cff14a558b69bcdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089743"
---
# <span data-ttu-id="059ce-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="059ce-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="059ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="059ce-102">SYNOPSIS</span></span>
<span data-ttu-id="059ce-103">Inaktiverar bara Azure AD-serverautentisering för en viss SQL Server.</span><span class="sxs-lookup"><span data-stu-id="059ce-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="059ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="059ce-104">SYNTAX</span></span>

```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="059ce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="059ce-105">DESCRIPTION</span></span>
<span data-ttu-id="059ce-106">Cmdleten **disable-AzSqlServerActiveDirectoryOnlyAuthentication** inaktiverar Azure Active Directory (Azure AD)-autentiseringskrav endast för en AzureSQL-server i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="059ce-106">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="059ce-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="059ce-107">EXAMPLES</span></span>

### <span data-ttu-id="059ce-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="059ce-108">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

<span data-ttu-id="059ce-109">Det här kommandot inaktiverar bara Azure Active Directory (Azure AD)-autentiseringskrav för en AzureSQL-server som heter Server01 som är kopplad till en resurs grupp med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="059ce-109">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="059ce-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="059ce-110">PARAMETERS</span></span>

### <span data-ttu-id="059ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059ce-111">-DefaultProfile</span></span>
<span data-ttu-id="059ce-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="059ce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059ce-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="059ce-113">-ResourceGroupName</span></span>
<span data-ttu-id="059ce-114">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="059ce-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="059ce-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="059ce-115">-ServerName</span></span>
<span data-ttu-id="059ce-116">Namnet på Azure SQL Server-administratören för Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="059ce-116">The name of the Azure SQL Server the Azure Active Directory administrator is in.</span></span>

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

### <span data-ttu-id="059ce-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="059ce-117">-Confirm</span></span>
<span data-ttu-id="059ce-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="059ce-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059ce-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="059ce-119">-WhatIf</span></span>
<span data-ttu-id="059ce-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="059ce-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="059ce-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="059ce-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059ce-122">CommonParameters</span></span>
<span data-ttu-id="059ce-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="059ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059ce-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="059ce-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059ce-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="059ce-125">INPUTS</span></span>

### <span data-ttu-id="059ce-126">System. String</span><span class="sxs-lookup"><span data-stu-id="059ce-126">System.String</span></span>

## <span data-ttu-id="059ce-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="059ce-127">OUTPUTS</span></span>

### <span data-ttu-id="059ce-128">Microsoft. Azure. commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="059ce-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="059ce-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="059ce-129">NOTES</span></span>

## <span data-ttu-id="059ce-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="059ce-130">RELATED LINKS</span></span>

[<span data-ttu-id="059ce-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="059ce-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="059ce-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="059ce-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="059ce-133">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="059ce-133">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="059ce-134">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="059ce-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
