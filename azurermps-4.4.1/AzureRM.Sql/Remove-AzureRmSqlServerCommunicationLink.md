---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 63bfce9b6f0d6aaa97fede65d8c96ac9079be349
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757982"
---
# <span data-ttu-id="67654-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="67654-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="67654-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67654-102">SYNOPSIS</span></span>
<span data-ttu-id="67654-103">Tar bort en kommunikations länk för elastiska databas transaktioner mellan två servrar.</span><span class="sxs-lookup"><span data-stu-id="67654-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67654-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67654-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67654-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67654-105">DESCRIPTION</span></span>
<span data-ttu-id="67654-106">Cmdleten **Remove-AzureRmSqlServerCommunicationLink** tar bort en länk för en server-till-server-kommunikation för elastiska databas transaktioner i Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="67654-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="67654-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67654-107">EXAMPLES</span></span>

### <span data-ttu-id="67654-108">Exempel 1: ta bort en kommunikations länk</span><span class="sxs-lookup"><span data-stu-id="67654-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="67654-109">Det här kommandot tar bort en länk för server-till-server-kommunikation med namnet Link01 på ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="67654-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="67654-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67654-110">PARAMETERS</span></span>

### <span data-ttu-id="67654-111">-Force</span><span class="sxs-lookup"><span data-stu-id="67654-111">-Force</span></span>
<span data-ttu-id="67654-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="67654-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="67654-113">-LinkName</span><span class="sxs-lookup"><span data-stu-id="67654-113">-LinkName</span></span>
<span data-ttu-id="67654-114">Anger namnet på den server kommunikation som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="67654-114">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="67654-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67654-115">-ResourceGroupName</span></span>
<span data-ttu-id="67654-116">Anger namnet på den resurs grupp som servern som anges av parametern *servername* tillhör.</span><span class="sxs-lookup"><span data-stu-id="67654-116">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="67654-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="67654-117">-ServerName</span></span>
<span data-ttu-id="67654-118">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="67654-118">Specifies the name of a server.</span></span>
<span data-ttu-id="67654-119">Den här servern innehåller den kommunikations länk som tas bort med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="67654-119">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="67654-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="67654-120">-Confirm</span></span>
<span data-ttu-id="67654-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="67654-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67654-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67654-122">-WhatIf</span></span>
<span data-ttu-id="67654-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="67654-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67654-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="67654-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67654-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67654-125">-DefaultProfile</span></span>
<span data-ttu-id="67654-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67654-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67654-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67654-127">CommonParameters</span></span>
<span data-ttu-id="67654-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67654-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67654-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67654-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67654-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67654-130">INPUTS</span></span>

## <span data-ttu-id="67654-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67654-131">OUTPUTS</span></span>

### <span data-ttu-id="67654-132">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="67654-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="67654-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67654-133">NOTES</span></span>
* <span data-ttu-id="67654-134">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, SQL, databas, MSSQL</span><span class="sxs-lookup"><span data-stu-id="67654-134">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="67654-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67654-135">RELATED LINKS</span></span>

[<span data-ttu-id="67654-136">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="67654-136">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="67654-137">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="67654-137">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="67654-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="67654-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)